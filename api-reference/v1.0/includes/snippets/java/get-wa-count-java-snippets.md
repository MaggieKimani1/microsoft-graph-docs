---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new HeaderOption("ConsistencyLevel", "eventual"));
requestOptions.add(new QueryOption("$orderby", "displayName "));
requestOptions.add(new QueryOption("$search", "displayName:wa"));

IUserCollectionPage users = graphClient.users()
	.buildRequest( requestOptions )
	.get();

```