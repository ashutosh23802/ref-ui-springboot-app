# ref-ui-springboot-app


Steps to create app:

1] Create a project from springboot intilizer.
2] Add a build.gradle at root.
3] add springboot generated project under backend
4] add angular generate project under frontend
5] Add setting.gradle and now tell Gradle the name of our project and make sure it will recognize the two modules.
6] Add build.gradle to frontend(ui).
7] Add below line to the backend build.gradle to include the ui project.
        dependencies {
        implementation(project(':todo-ui'))
        }

8] add gradle task dependency like below

afterEvaluate {
	processResources.dependsOn ':frontend:copyArtifact'
}
