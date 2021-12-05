for v2.4.2

Clone to folder: <Magento install>/app/code/Magestore/
Module Name: Magestore_Quotation

php bin/magento module:enable Magestore_Quotation
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy -f
php bin/magento indexer:reindex
php bin/magento c:c
php bin/magento deploy:mode:show
php bin/magento deploy:mode:set developer
php bin/magento deploy:mode:set production

sudo systemctl restart apache2
curl -X GET 'http://localhost:9200'
