# Helix.VsTemplates
Templates for use with LaubPlusCo.Helix.VsTemplates Visual Studio extension

Custom configured templates for use with [LaubPlusCo.Helix.VsTemplates](https://github.com/LaubPlusCo/LaubPlusCo.Helix.VsTemplates) Visual Studio extension.

## Changes from original
* template.manifest.xml
    * $sitecoreVersion$ token updated to 8.2.170614 (8.2 Update 4)
* *.csproj 
    * `<TargetFrameworkVersion>v4.6.1</TargetFrameworkVersion>`
    * `<HintPath>` updated to 8.2.170614
    * Added new ItemGroup to include Unicorn .yml files for use with [RainbowDataAnalyzer](https://github.com/hermanussen/RainbowDataAnalyzer)
    ````
        <ItemGroup>
          <AdditionalFiles Include="..\serialization\**\*.yml">
            <Visible>false</Visible>
          </AdditinonalFiles>
        </ItemGroup>
    ````
    * Remove: Templates.cs
* packages.config
    * Add Glass.Mapper.Sc.Core
    * Add Castle.Core
* *.Serialization.config
    * `<targetDataStore physicalRootPath="$(sourceFolder)\...`
* Add Models folder
* Views/web.config
    * `<add namespace="Sitecore.Mvc" />`
* HabitatStyle.Project.Module
    * `App_Config/Include/Project` instead of `App_Config/Include/Feature`
