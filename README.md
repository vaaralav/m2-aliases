# m2-aliases
Some shell aliases to make Magento 2 development a little more comfortable.

```shell
alias m2permissions='echo "Setting M2 permissions for magento installation at \"`pwd`\"..." && sudo find var vendor pub/static pub/media app/etc -type f -exec chmod g+w {} \; && sudo find var vendor pub/static pub/media app/etc -type d -exec chmod g+ws {} \; && sudo chown -R :www-data . && chmod u+x bin/magento'
alias m2upgrade='php bin/magento setup:upgrade'
alias m2compile='php bin/magento setup:di:compile'
alias m2reindex='php bin/magento indexer:reindex'
alias m2='php bin/magento'
```

## Examples
### Upgrading a module or getting started with some project

```shell
m2upgrade && m2compile && m2permissions
```

### Clear cache

```shell
m2 cache:clean
```
