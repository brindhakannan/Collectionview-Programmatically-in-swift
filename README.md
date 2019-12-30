# Collectionview-Programmatically-in-swift

            let layout = UICollectionViewFlowLayout()
            layout.scrollDirection = UICollectionView.ScrollDirection.horizontal
            //layout.scrollDirection = UICollectionView.ScrollDirection.vertical
            
            coll_view = UICollectionView(frame: .zero, collectionViewLayout: layout)
            coll_view.setCollectionViewLayout(layout, animated: true)
            coll_view.translatesAutoresizingMaskIntoConstraints = false
            view.addSubview(coll_view)
            coll_view.leadingAnchor.constraint(equalTo: view.leadingAnchor, constant: 10).isActive = true
            coll_view.trailingAnchor.constraint(equalTo: view.trailingAnchor, constant: -10).isActive = true
            coll_view.topAnchor.constraint(equalTo: view.topAnchor, constant: 10).isActive = true
            coll_view.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -10).isActive = true
            coll_view.backgroundColor = .lightGray
            coll_view.register(CollectionViewCell.self, forCellWithReuseIdentifier: "CollectionViewCell")
            coll_view.delegate = self
            coll_view.dataSource = self
            coll_view.reloadData()
