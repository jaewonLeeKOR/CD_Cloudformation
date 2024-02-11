# Terraform
하시코프에서 Go 언어로 개발한 오픈소스 IaC(Infrastructure as Code) 도구

## Terraform Code 의 구성
- Terraform 코드는 `.tf` 로 끝남

|파일|설명|
|:--:|:--:|
|main.tf|리소스를 구축하는 부분|
|variables.tf|사용자가 사용할 수 있는 변수를 정의하는 부분|
|output.tf|성공적인 Terraform이 실행되고 난 후 표시될 출력|
|provider.tf|프로바이더 버전 및 프로바이더 구성 정의|

## Terraform Init
- Terraform으로 작업하기 위해서는 Workspace를 초기화 해야함
```
terraform init
```
- `terraform init` 명령은 Terraform 코드를 스캔하고 필요한 Provider를 식별한 후 다운로드 함
- 성공시 다음과 같은 출력이 생김

  <img width="645" alt="image" src="https://github.com/jaewonLeeKOR/IaC/assets/58386334/402681fd-3e94-4935-bcbd-b9eb3f80fc66">
- AWS Provider는 `.terraform/providers/registry.terraform.io/hashicorp` 경로에 설치됨
- https://registry.terraform.io/namespaces/hashicorp 에서 Provider를 확인 가능
