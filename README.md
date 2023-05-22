# redis-sentinelpool
基于jedis-sentinelpool扩展，支持读写分离
应用场景：应对少量数据的高吞吐量性能要求，比如品牌电商（小米、华为手机）的爆款商品秒杀活动，数据量不大，但读写请求高。
原理：将哨兵模式优化为读写分离，slave节点作为读节点，可无限扩展。
测试：8c8g部署redis，tps读3w，写2w。
