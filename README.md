wal-e
=========

    Install and configure wal-e


Role Variables
--------------

    wale_install: true              [ true | false ] for install wal-e
    wale_cronjob: false             [ true | false ] for create daily full backup cronjob
    wale_postgresql_version         [ required ] postgresql version
    wale_aws_access_key_id: ''      [ required ] aws access key id
    wale_aws_secret_access_key: ''  [ required ] aws secret access key 
    wale_aws_s3_endpoint: ''        [ required ] aws s3 endpoint
    wale_aws_s3_prefix: ''          [ required ] aws s3 prefix

Example Playbook
----------------

    - hosts: server
      vars:
        wale_aws_access_key_id: ''
        wale_aws_region: ''
        wale_aws_secret_access_key: ''
        wale_s3_prefix: ''
        wale_postgresql_version: 10
      roles:
      - { role: wale, tags: wale }

License
-------

    MIT

Author Information
------------------

    Dmitrij Petrov
