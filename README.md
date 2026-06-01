# Jenkins CI/CD Pipeline

A Jenkins declarative pipeline template demonstrating a complete **CI/CD workflow** with stages for Setup, Build, Test, Package, and Deploy.

## Pipeline Stages

```
Setup → Build → Test → Package → Deploy
```

| Stage | Description |
|---|---|
| Setup | Environment initialization |
| Build | Compile / build the application |
| Test | Run unit and integration tests |
| Package | Package the artifact |
| Deploy | Deploy to target environment |

## Files

| File | Description |
|---|---|
| `Jenkinsfile` | Declarative pipeline definition |
| `app.java` | Sample Java application |
| `style.css` | Frontend styles |

## How to Use

1. Set up a Jenkins server (local or cloud)
2. Create a new **Pipeline** job in Jenkins
3. Point it to this repository
4. Jenkins will automatically pick up the `Jenkinsfile`
5. Replace the `echo` placeholders in each stage with your actual build/test/deploy commands

## Pipeline Structure

```groovy
pipeline {
    agent any
    stages {
        stage("Setup")   { ... }
        stage("Build")   { ... }
        stage("Test")    { ... }
        stage("Package") { ... }
        stage("Deploy")  { ... }
    }
    post {
        always  { /* cleanup */ }
        success { /* notify */ }
        failure { /* alert  */ }
    }
}
```

## Screenshots

![Pipeline View](Screenshot%20(13).png)
![Build Output](Screenshot%20(14).png)
