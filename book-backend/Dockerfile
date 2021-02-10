# jDK를 다운받는다
FROM openjdk:8-jdk-alpine 

# /app폴더를 만든다.
WORKDIR /app
# 변수 설정 = 타켓 폴더에 *(모든이름의).jar 파일을 설정한다.
ARG JAR_FILE=target/*.jar
# 그 jar파일을 app.jar파일로 바꿔서 저장해라.
COPY ${JAR_FILE} app.jar
# 8080 포트를 외부에서 접근 가능 하도록 설정.
EXPOSE 8080
# 프로파일 설정 (active = prod로 하면 MySQL이 없기 때문에 안된다.)
ENTRYPOINT ["java", "-Dspring.profiles.active=dev", "-jar", "app.jar"]