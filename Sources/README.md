# 폴더설명
# 1.Sources: 프로젝트의 모든 Swift 소스파일을 포함
1.1. Sources/App: 앱을 구성하는데 필요한 코드를 포함
1.1.1 Sources/App/Controllers: 로직을 그룹화하는 컨트롤러가 위치
1.1.2 Sources/App/Migrations: 데이터베이스 마이그레이션을 정의하는 타입이 위치
1.1.2 Sources/App/Models: 데이터베이스의 데이터 구조를 나타내는 모델이 위치
1.1.3 Sources/App/configure.swift: 앱을 구성하는 configure(_: ) 함수를 포함함.
                            main.swift파일에 의해 호출되며 
                            이 함수에 라우트나 데이터베이스 등의 서비스를 등록해야 한다.
1.1.4 Sources/App/routes.swift: 앱에 라우트를 등록하는 route(_:)함수를 포함하며 
                            configure(_:)함수에 의해 호출
                            
1.2. Sources/Run: 앱을 실행하는데 필요한 코드만 포함
1.2.1 Sources/Run/main.swift: 앱의 인스턴스를 생성하고 실행

# 2. Tests: XCTVapor모듈을 사용하는 단위테스트를 포함

-----
Vapor의 핵심적인 프레임워크 두 가지

SwiftNIO
Vapor는 Apple에서 만든 SwiftNIO 프레임워크를 기반으로 설계되었음. 
SwiftNIO는 비동기 네트워킹 프레임워크로, Vapor의 모든 HTTP 통신을 처리. 
Vapor가 요청을 받고 응답을 보낼 수 있게 하며, 연결 및 데이터 전송을 관리.
Vapor의 일부 API는 EventLoopFuture 제네릭 타입을 반환. 
EventLoopFuture는 나중에 제공될 결과에 대한 플레이스홀더.
비동기적으로 동작하는 함수는 실제 데이터를 즉시 반환하지 않고, 대신 EventLoopFuture를 반환.

Fluent
Fluent는 Swift 용 ORM(Object-relational mapping) 프레임워크. 
Vapor 앱과 데이터베이스 사이의 추상화 계층으로, 데이터베이스를 쉽게 사용할 수 있도록 인터페이스를 제공. 
따라서 SQL을 작성하지 않고도 Swift로 데이터베이스 작업을 수행할 수 있음.
 







