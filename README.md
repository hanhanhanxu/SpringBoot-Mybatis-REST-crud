<a href="https://996.icu"><img src="https://img.shields.io/badge/link-996.icu-red.svg" alt="996.icu" /></a>

# SpringBoot-Mybatis-REST-crud
sprngboot整合mybatis，使用swagger接口文档，crud工程


> 这几天才知道原来restfull风格需要严格控制controller中的返回类型，需要是ReponseEntity<T>类，好像是这个吧忘记了。后面会出严谨的restful风格工程。

想了想我对restful风格的理解过程：
- 最开始：只要符合访问链接url：xxx/xxx/xxx/x之类的即可。springmvc拦截所有/，controller中全部是@RequestMapping,参数使用@PathVariable，这样保证了url后缀不是.jsp或.html，而是斜杠斜杠的，以为这就是restful风格
（拦截所有时静态路径放行：在springmvc中配置两个mvc啥啥标签）

- 其次：以为加上请求类型就行了。@PostMapping，@DeleteMapping，@PutMapping，@GetMapping。统一返回对象不再使用视图解析器返回到jsp或者html。
（前后端分离，ajax进行前后台数据异步交互。可以让controller类继承一个包装类BaseController，就能统一返回一个类型了）

- 现在：返回ReponseEntity<T>类
