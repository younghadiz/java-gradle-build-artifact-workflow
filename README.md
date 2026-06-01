# Java Gradle Build Artifact Workflow

## Project Overview

This project demonstrates a production-style Java build workflow using Gradle.

The objective is to understand how DevOps engineers interact with application source code, build tools, automated testing, artifact generation, runtime validation, and version control workflows before software is released or deployed.

---

## Learning Objectives

This project demonstrates:

* Cloning an existing Java Gradle project
* Creating personal GitHub and GitLab repositories
* Working with `main`, `develop`, and `feature/*` branches
* Preserving Git history using non-fast-forward merges
* Running Gradle tests
* Investigating and fixing build failures
* Cleaning build directories
* Building executable JAR artifacts
* Running Java applications from generated artifacts
* Passing runtime parameters to Java applications
* Validating builds on a Linux server
* Following production-style DevOps workflows

---

## Technology Stack

| Technology   | Purpose                       |
| ------------ | ----------------------------- |
| Java         | Application Language          |
| Gradle       | Build Automation Tool         |
| Git          | Version Control               |
| GitHub       | Primary Portfolio Repository  |
| GitLab       | Secondary Backup Repository   |
| Ubuntu Linux | Server Validation Environment |
| DigitalOcean | Cloud Infrastructure          |

---

## Architecture Diagram

```text
Developer Workstation
        |
        | Clone Source Project
        v
Local Java Gradle Repository
        |
        | Feature Branch Development
        v
Gradle Test & Build Workflow
        |
        | ./gradlew test
        | ./gradlew clean build
        v
Generated JAR Artifact
        |
        | java -jar
        v
Runtime Validation
        |
        | git push
        v
GitHub + GitLab Repositories
        |
        | git clone
        v
Ubuntu Server Validation
        |
        | Build Verification
        v
Portfolio Evidence
```

---

## Git Workflow

```text
main
  |
  └── develop
        |
        ├── feature/build-jar-check
        ├── feature/fix-test
        ├── feature/clean-build
        ├── feature/run-jar
        └── feature/application-parameters
```

---

## Gradle Commands Used

### Run Tests

```bash
./gradlew test
```

### Clean Build Directory

```bash
./gradlew clean
```

### Build Application

```bash
./gradlew build
```

### Production Style Build

```bash
./gradlew clean build
```

This command:

1. Removes previous build artifacts
2. Runs all tests
3. Compiles the application
4. Generates the JAR artifact

---

## Running the JAR Artifact

### Execute Application

```bash
java -jar build/libs/app-1.0.jar
```

### Execute Application with Parameters

```bash
java -jar build/libs/app-1.0.jar hello devops
```

---

## DigitalOcean Ubuntu Server Validation

### Install Dependencies

```bash
sudo apt update

sudo apt install -y \
git \
curl \
unzip \
openjdk-17-jdk
```

### Clone Repository

```bash
git clone https://github.com/younghadiz/java-gradle-build-artifact-workflow.git

cd java-gradle-build-artifact-workflow
```

### Make Gradle Wrapper Executable

```bash
chmod +x gradlew
```

### Run Tests

```bash
./gradlew test
```

### Build Artifact

```bash
./gradlew clean build
```

### Execute Application

```bash
java -jar build/libs/app-1.0.jar server validation
```

---

## Repository Structure

```text
java-gradle-build-artifact-workflow/
├── src/
│   ├── main/
│   └── test/
├── gradle/
├── gradlew
├── gradlew.bat
├── build.gradle
├── settings.gradle
└── README.md
```

---

## Security Notes

Never commit the following files or credentials:

* SSH private keys
* GitHub Personal Access Tokens
* GitLab Access Tokens
* DigitalOcean API Tokens
* Cloud credentials
* `.env` files
* Database passwords
* Server passwords
* Private certificates

---

## DevOps Lessons Learned

This project demonstrates how DevOps engineers support software delivery by understanding:

* Source code management
* Branching strategies
* Automated testing
* Build automation
* Artifact generation
* Runtime validation
* Linux-based execution environments

A DevOps engineer may not develop most application features, but must understand how software is built, tested, packaged, validated, and prepared for deployment.

---

## Future Improvements

* Add Jenkins CI pipeline
* Add GitHub Actions workflow
* Add Docker containerization
* Add automated artifact publishing
* Add SonarQube code quality scanning
* Add Nexus artifact repository integration

---

## Author

**Gafari Salaudeen**

DevOps Practitioner
