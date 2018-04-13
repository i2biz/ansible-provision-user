Role Name
=========

Simply set SSH user, allow him paswordless sudo, and 
configure ssh keys.  

Use this to create unpredictable provisioning user name and then (or just use this for all your admins): 

* Give provision user paswordless sudo; 
* Add predefined authorized keys; 
* Disable remote access for all other users; 

Requirements
------------

Not much, tested on recent debian. 

Role Variables
--------------

    # Provision user name
    provision_user_name: "provision"
    # Set this to contents to ``authorized_keys`` file
    provision_user_authorized_keys: | 
       rsa-something key 
       ecdsa-something key     
    # Provision user password, by default "!" which blocks password login.  
    provision_user_password: "!"

License
-------

BSD
