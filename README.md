Provides Postgres Hstore Type for Doctrine2
-------------------------------------------
Provides Doctrine Type class for postgres hstore type

#### Using with Zend Framework 2

Add this to `config\autoload\global.php`

    <?php

    return array(
        'doctrine' => array(
            'connection' => array(
                'orm_default' => array(
                 ...
                )
            ),
            'configuration' => array(
                'orm_default' => array(
                    'types' => array(
                        'hstore' => 'YouProjectNamespace\Doctrine\Types\HstoreType'
                    )
                )
            )
        )
     );

Usage in Entity class

     <?php

     /**
      * Class SuperEntity
      * @Entity
      * @Table(name="super-table")
      */
     class SuperEntity
     {
         /**
          * @var int
          *
          * @Id @Column(type="integer")
          * @GeneratedValue
          */
         private $id;

         /**
          * @var mixed
          *
          * @Column(name="inputs", type="hstore")
          */
         private $inputs;

#### License

Licensed under the MIT License