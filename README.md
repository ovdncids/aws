# AWS
https://aws.amazon.com

# 자습서
https://aws.amazon.com/ko/getting-started/tutorials

# 콘솔
https://console.aws.amazon.com/console/home

# IAM
https://console.aws.amazon.com/iam

# 웹 호스팅
https://aws.amazon.com/ko/websites

# S3
https://aws.amazon.com/ko/s3

해당 파일에 접근 방법
```
개요 > 해당 파일 클릭 > 링크 클릭
```

## AWS Command Line Interface 설치
https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/installing.html

```sh
# 설치
pip install awscli --upgrade --user
# 버전 보기
aws --version
```

PATH가 걸려 있지 않는다는 에러가 나올 경우
```sh
vi ~/.bash_profile

# Python3 경로 추가
export PATH=${PATH}:/Users/유저/Library/Python/3.7/bin
```

```sh
# .bash_profile 다시 부르기
source ~/.bash_profile

# pip로 다시 설치 한다.
pip install awscli --upgrade --user
```

## S3에서 IAM 사용
https://aws.amazon.com/ko/getting-started/tutorials/backup-to-s3-cli/

### AWS CLI S3 사용중 에러가 발생할 경우
https://lovemewithoutall.github.io/it/aws-cli-configure/

# Lambda
https://aws.amazon.com/ko/lambda

# Amplify Framework
https://aws-amplify.github.io/docs

## Amplify Framework 설치
```sh
npm install -g @aws-amplify/cli
amplify configure
  # 리전을 ap-northeast-1으로 설정한다.
```

## Amplify 초기화
```sh
# 도움말
amplify
# 초기화
amplify init
  # Build Command: npm run-script build
  # Start Comand: npm run-script start
  # Do you want to use an AWS profile? Yes
    # 이미 amplify configure에서 설정한 profile을 사용한다.
# 현재 amplify에 리소스 무엇이 설치 되어 있는지 볼 수 있다.
amplify status
# 모든 리소스를 업데이트 하고 로컬을 실행 시킨다.
# aws-exports.js 파일이 생성된다.
amplify serve
# 분석 카테고리 리소스를 설치 한다.
amplify add analytics
# 클라우드에 올린다.
amplify push
# 로컬 빌드 후에 클라우드에 올린다.
amplify publish
# 현재 설정된 API 카테고리를 수정 한다.
amplify update api
# 해당 카테고리를 지운다.
amplify remove api
# API 콘솔 페이지로 이동
amplify console api
```

## Amplify Javascript 연동
https://aws-amplify.github.io/docs/js/start
https://aws-amplify.github.io/docs/js/api

## Amplify 프로젝트 생성

### Auth
```
No, I will set up my own configuration.
User Sign-Up & Sign-In only (Best used with a cloud API only)

Please provide a friendly name for your resource that will be used to label this category in the project: scoreviewer
Please provide a name for your user pool: scoreviewer_user_pool

MFA: OFF
Enabled (Requires per-user email entry at registration)

Please specify an email verification subject: Enter
lease specify an email verification message: Enter
Do you want to override the default password policy for this User Pool? N
Userpool users are created with a standard set of attributes defined by the OpenID Connect specification: 선택 안 함

Specify the app's refresh token expiration period (in days): 30
Do you want to specify the user attributes this app can read and write? N
```

### DynamoDB
테이블을 미리 만든다.

### API
```
REST
Provide a friendly name for your resource to be used as a label for this category in the project: scoreviewer
Provide a path (e.g., /items) /scores

Create a new Lambda function
Provide a friendly name for your resource to be used as a label for this category in the project: scoreviewer
Provide the AWS Lambda function name: scoreviewer
CRUD function for Amazon DynamoDB table (Integration with Amazon API Gateway and Amazon DynamoDB)
Use a DynamoDB table already deployed on AWS
만들어져 있는 테이블 선택

Do you want to edit the local lambda function now? Y
Restrict API access: Y
Authenticated users only
read/write
Do you want to add another path? N
```

### JSON 웹 토큰 확인
```
https://cognito-idp.{region}.amazonaws.com/{userPoolId}/.well-known/jwks.json
```

# 리전
https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/using-regions-availability-zones.html

## 리전 속도 측정
https://www.cloudping.info

http://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html

## 도쿄 리전
AP-NORTHEAST-1

## 서울 리전
AP-NORTHEAST-2

## 이전 배포
https://d2nfsbmw1bdqln.cloudfront.net

## Events 사용량
https://console.aws.amazon.com/pinpoint/home/?region=us-east-1#/apps/51fb001a4da54fabad43ec4403e28ffe/analytics/events

# GraphQL
https://graphql.github.io/

## demo
https://github.com/graphql/graphiql

# AppSync
https://console.aws.amazon.com/appsync

# DynamoDB
https://console.aws.amazon.com/dynamodb

# CloudFormation
https://console.aws.amazon.com/cloudformation/

클라우드 전체를 관리하는듯 하다.

# Cognito (사용자 풀)
https://console.aws.amazon.com/cognito

## JSON 웹 토큰 확인 방법
https://docs.aws.amazon.com/ko_kr/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-verifying-a-jwt.html

# 모든 서비스
전역
  S3, IAM
리전
  Cognito,
  AppSync(GraphQL),
  Lambda,
  DynamoDB
  CloudFormation
