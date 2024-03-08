##使用缓存提高服务性能。
下面采用伪代码来表达。针对电商查询商品详情，或者商品信息的场景。
1.都先从db获取商品信息，getProductFormDb(Long projectId);为了避免每次查询商品都请求到db，导致db压力过大，所以将商品信息缓存起来。那么可以借助redis进行数据缓存。
2.将商品放入缓存，redisService.set();
