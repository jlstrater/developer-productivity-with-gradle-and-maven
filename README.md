# Developer Productivity with Gradle and Maven

As presented at the Münster JUG on July 10. Slides are published [here](https://jlstrater.github.io/developer-productivity-with-gradle-and-maven/#/).


## Running This Presentation

This is a project using @melix's Asciidoctor+Reveal.js template presentations. If you want to use it for yourself, just fork this repository and update the presentation as you wish.

### Configuration

Minimally, update the `build.gradle.kts` file to set your GitHub username:

```
presentation {
    githubUserName.set("yourUserName")
}
```

and change the name of the project in `settings.gradle.kts`:

```
rootProject.name = "my-awesome-presentation"
```

### Generating the presentation

Run:

```
./gradlew asciidoctor
```

### Uploading the slides on GitHub pages

Run:

```
./gradlew publishGhPages
```

If your repository name is different from the name of the project in `settings.gradle.kts`, update the configuration in `build.gradle.kts`:

```
presentation {
    githubUserName.set("yourUserName")
    githubRepoName.set("yourRepoName")
}
```

Then the presentation is going to be available at `https://yourUserName.github.io/yourRepoName/`

### Exporting the presentation

This template supports exporting the presentation to PDF, JPEG and PNG.
You'll need a JDK which bundles JavaFX to do this.
Run this task:

```
./gradlew exportToPdf
```

to generate a PDF, or:

```
./gradlew export
```

to export to all formats.
