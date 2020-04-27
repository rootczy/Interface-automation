# Interface-automation
- 基于Java语言的接口自动化从0-1的落地实践
- mock-runner使用说明

- 1.什么是mock
    - Moco 是一个搭建模拟服务器的工具，其支持 API 和独立运行两种方式，前者通常是在 junit 、testng等测试框架中使用，后者则是通过运行一个 jar 包开启服务。

- 2.Moco在开发中会起到的作用
    - Moco是针对HTTP集成而生的，不过，现在也有人把它用在其它需要一个模拟服务器的场景中。比如，在移动开发中，有人开发一个移动应用，需要有一个远端服务，但在开发时，这个服务还不存在，他就用Moco模拟了一个服务，保证移动应用可以顺利的开发。
    - 同样，也有人把它用在Web前端开发里，当我们的页面需要通过与服务器交互时，就可以用Moco模拟这样一个服务。这种做法在开发一个页面原型时，非常有用，因为那个时候，我们还来不及开发一个完整的服务。
   
- 3.Moco在接口测试中的用处
    - 既然开发人员可以通过 Moco 模拟一个还不存在的服务来进行开发、调试，那对于接口测试来说，也可以模拟一个服务进行测试。
   - 一般而言，在项目的接口文档输出后，开发人员会进行接口开发工作，测试人员会进行接口用例的设计，但往往完成用例设计会先于接口开发工作，此时如果要进行接口用例的执行，则前提是开发人员完成接口开发工作。
   - 而通过 Moco 框架，就可以在接口文档输出后，在接口开发、接口用例设计的同时，使用 Moco 搭建一个模拟服务器，这样在用例设计完成后，即使接口开发工作还未完成，也可以立即进行执行接口用例，在这个过程中可以修改、补充用例，如此的话，在接口开发完成以后，只需要简单的去执行所有的用例就 OK，省去了很大的工作量，并且这些完善的用例，用自动化去执行，效果更佳。
 
- 4.Moco的应用 演示示例
    - 4.1.模拟get请求
    
    - 4.2.模拟带参数的get请求

    - 4.3.模拟post请求

    - 4.4.模拟带form格式参数的post请求

    - 4.5.模拟request请求中带cookies信息的get请求

    - 4.6.模拟request请求中带cookies的post请求，post请求带json格式参数，返回结果也使用json格式

    - 4.7.模拟response返回中带有cookies信息的get请求

    - 4.8.模拟带有headers信息的mock请求

    - 4.9.模拟有重定向的接口

    - 4.10使用httpclient调moco的接口
- 以上示例代码在src.resource.mock.sample包下
    - 运行命令
```
java -jar moco-runner-0.11.0-standalone.jar http -p 8081 -c have-Paramatersget.json

```


