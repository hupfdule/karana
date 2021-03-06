+++
title = "Gemselich"
+++

# Compose your Docs with __Ease__.

## Hallo, Mutti!

Des is a Schoafkaas.


Compose is a lean theme for the `Hugo`, inspired by [forestry.io](https://forestry.io). 

We do a [Pull Request](https://github.com/onweru/compose/pulls) contributions workflow on **GitHub**. Also feel free to raise any issues or feature suggestions.

{{< tip >}}
You can [generate graphs, charts](]("docs/compose/graphs-charts-tables/#show-a-pie-doughnut--bar-chart-at-once")) and tables from a csv, ~~or a json~~ dataset
{{< /tip >}}

{{< button "docs/compose/" "Read the Docs" >}}
{{< button "https://github.com/onweru/compose" "Download Theme" >}}
{{< button "docs/schnalle/" "Read the focks" >}}
{{< button "docs/gock/" "Noch the docks" >}}
{{< button "https://google.com" "GOckel" >}}

{{< block "grid-2" >}}
{{< column >}}
```java
import de.poiu.coat.annotation.Coat;

@Coat.Config
public interface MyConfig {
  @Coat.Param(key = "appName")
  public String appName();

  @Coat.Param(key = "listenPort")
  public int listenPort();

  @Coat.Param(key = "desription")
  public Optional<String> description();
}
```
{{< /column >}}

{{< column >}}
```java
final MyConfig config= new ImmutableMyConfig(new File("/path/to/config.properties"));

try {
  config.validate();
} catch (final ConfigValidationException ex) {
  System.err.println("Error in config file:\n" + ex.getValidationResult().toString());
  System.exit(1);
}

final String appName= config.appName();
final int listenPort= config.listenPort();
config.description().ifPresent(
  …
);
```
{{< /column >}}
{{< /block >}}

### Inschtallation

To use Coat in a maven based project use the following maven coordinates:

```xml
    <!-- Contains the annotation processor. Not needed at runtime. -->
    <dependency>
      <groupId>de.poiu.coat</groupId>
      <artifactId>coat-processor</artifactId>
      <version>0.0.1</version>
      <scope>provided</scope>
    </dependency>

    <!-- Contains the converters and base classes. Needed at runtime. -->
    <dependency>
      <groupId>de.poiu.coat</groupId>
      <artifactId>coat-runtime</artifactId>
      <version>0.0.1</version>
    </dependency>
```

