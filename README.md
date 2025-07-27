# Library App

## Description

Library App은 도서관 회원, 도서, 대출 관리를 위한 콘솔 기반 C# 애플리케이션입니다. JSON 파일을 데이터 저장소로 활용하며, 회원 검색, 도서 대출/반납, 대출 연장, 회원권 갱신 등 도서관 운영에 필요한 주요 기능을 제공합니다.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- .vscode/
  - settings.json
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Program.cs
    - Json/
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
- tests/
  - UnitTests/
    - LoanFactory.cs
    - ...

## Key Classes and Interfaces

- **Library.ApplicationCore**
  - `Entities/` : 도메인 엔터티(Patron, Book, Loan 등)
  - `Enums/` : 대출/회원 관련 상태 Enum
  - `Interfaces/` : 데이터 접근 및 서비스 인터페이스(`IPatronRepository`, `ILoanRepository`, `IPatronService`, `ILoanService`)
  - `Services/` : 비즈니스 로직 서비스(`PatronService`, `LoanService`)

- **Library.Infrastructure**
  - `Data/JsonData` : JSON 파일 기반 데이터 로딩/저장 및 엔터티 참조 연결
  - `Data/JsonPatronRepository`, `Data/JsonLoanRepository` : Repository 인터페이스 구현체

- **Library.Console**
  - `ConsoleApp` : 콘솔 UI 상태 관리 및 사용자 상호작용 컨트롤러
  - `ConsoleState`, `CommonActions` : 상태 전이 및 공통 동작 정의

## Usage

1. 저장소를 클론합니다.
2. 솔루션 파일(AccelerateDevGitHubCopilot.sln)을 Visual Studio 또는 VS Code에서 엽니다.
3. 빌드하여 의존성을 복원합니다.
4. `Library.Console` 프로젝트를 실행합니다.
5. 안내에 따라 회원 검색, 상세 조회, 대출 연장, 반납, 회원권 갱신 등의 기능을 사용할 수 있습니다.

## License

This project is licensed under