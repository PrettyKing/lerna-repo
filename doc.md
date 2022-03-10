注意，子包的依赖也要在package.json中引入，进入子包目录，用yarn add的方式添加依赖。如果是根存在的公共依赖，不会安装，如果是独特的依赖，会单独引入（由于使用了yarn workspaces，会在根目录的node_modules统一安装）

依赖add完毕之后，在项目根目录运行yarn build:all或者yarn build:changed

就会发现子包根目录出现dist文件夹，这里面就是打包出来的文件。
运行yarn release

