# CardlinkSDK: Android Implementation Documentation

## Requirements

#### Android version : API level 30 or higher.

## Installation

#### Add the following dependency to your app’s build.gradle:

```
implementation 'de.ihreapotheken.sdk.cardlink:1.4.0'
```
#### Modify your settings.gradle:
```
dependencyResolutionManagement {
    repositories {
        maven {
            name = "GitHubPackages"
            url = uri("https://maven.pkg.github.com/ihreapotheken/CardLinkSDK-Android")
            credentials {
                username = System.getenv("GITHUB_USERNAME") ?: ""
                password = System.getenv("GITHUB_TOKEN") ?: ""
            }
        }
        maven {
            name = "Link4Health Nexus"
            url = uri("https://nexus.link4.health/repository/link4health-anonymous/")
            mavenContent {
                releasesOnly()
            }
        }
        google()
        mavenCentral()
    }
}
```
> 📌 **Note:** GitHub requires authentication to fetch packages, even from public repositories.
>
> **Generate a GitHub Token:**
> - Go to **[GitHub Personal Access Tokens](https://github.com/settings/tokens)**
> - Click **"Generate new token (classic)"**
> - Enable **`read:packages`** permission
> - Copy the generated token
> - Store credentials in your system’s environment variables
