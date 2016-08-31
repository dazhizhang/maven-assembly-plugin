# maven-assembly-plugin
maven导入其它project的类包

http://maven.apache.org/plugins/maven-assembly-plugin/usage.html

<project>
  [...]
  <build>
    [...]
    <plugins>
      <plugin>
        <artifactId>maven-assembly-plugin</artifactId>
        <version>2.6</version>
        <configuration>
          <descriptorRefs>
            <descriptorRef>jar-with-dependencies</descriptorRef>
          </descriptorRefs>
        </configuration>
        <executions>
          <execution>
            <id>make-assembly</id> <!-- this is used for inheritance merges -->
            <phase>package</phase> <!-- bind to the packaging phase -->
            <goals>
              <goal>single</goal>
            </goals>
          </execution>
        </executions>
      </plugin>
      [...]
	<dependencies>
		 <dependency>
		  <artifactId>need_to_imported_local_maven</artifactId> 
		  <groupId>localmaven</groupId> 
		  <version>1.0</version> 
		  </dependency>
	</dependencies>
</project>

