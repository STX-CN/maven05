依赖
A->B->C,那么A间接依赖C

如果C在pom.xml中同时依赖A和B，那么要遵循短路优先的原则，直接依赖B
如果路径相同
A->B
A->C
那么谁先声明，就依赖谁。

maven项目聚合，如maven05-demoABC将A,B,C项目聚合进来，同时编译
修改的地方:
1. 修改打包方式
<packaging>pom</packaging>

2. 添加打包进来的模块
  <modules>
  	<module>../maven05-demoA</module>
  	<module>../maven05-demoB</module>
  	<module>../maven05-demoC</module>
  </modules>









