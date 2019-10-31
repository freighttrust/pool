# Getting started

## How to Build

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

"This library requires Visual Studio 2017 for compilation."
1. Open the solution (BlockarrayNetwork.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the BlockarrayNetwork library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

### 3. Add reference of the library project

In order to use the BlockarrayNetwork library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` BlockarrayNetwork.Standard ``` and click ``` OK ```. By doing this, we have added a reference of the ```BlockarrayNetwork.Standard``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=blockarray-network-CSharp&workspaceName=BlockarrayNetwork&projectName=BlockarrayNetwork.Standard)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### 

API client can be initialized as following.

```csharp

BlockarrayNetworkClient client = new BlockarrayNetworkClient();
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SystemController](#system_controller)
* [ItBlockarrayComDriverController](#it_blockarray_com_driver_controller)
* [ItBlockarrayComShipperController](#it_blockarray_com_shipper_controller)
* [ItBlockarrayComCarrierController](#it_blockarray_com_carrier_controller)
* [ItBlockarrayComReceiverController](#it_blockarray_com_receiver_controller)
* [ItBlockarrayComDriverPassportController](#it_blockarray_com_driver_passport_controller)
* [ItBlockarrayComAddDriverController](#it_blockarray_com_add_driver_controller)
* [ItBlockarrayComCreateDriverPassportController](#it_blockarray_com_create_driver_passport_controller)
* [ItBlockarrayComUpdateDriverPassportController](#it_blockarray_com_update_driver_passport_controller)
* [ItBlockarrayComChangeDriverCarrierController](#it_blockarray_com_change_driver_carrier_controller)
* [ItBlockarrayComRemoveDriverCarrierController](#it_blockarray_com_remove_driver_carrier_controller)
* [ItBlockarrayComDetentionController](#it_blockarray_com_detention_controller)
* [ItBlockarrayComQuoteController](#it_blockarray_com_quote_controller)
* [ItBlockarrayComLoadController](#it_blockarray_com_load_controller)
* [ItBlockarrayComAssignDriverToLoadController](#it_blockarray_com_assign_driver_to_load_controller)
* [ItBlockarrayComOriginArrivalController](#it_blockarray_com_origin_arrival_controller)
* [ItBlockarrayComLoadPickupController](#it_blockarray_com_load_pickup_controller)
* [ItBlockarrayComDestinationArrivalController](#it_blockarray_com_destination_arrival_controller)
* [ItBlockarrayComLoadDropOffController](#it_blockarray_com_load_drop_off_controller)
* [ItBlockarrayComListLoadController](#it_blockarray_com_list_load_controller)
* [ItBlockarrayComSubmitQuoteController](#it_blockarray_com_submit_quote_controller)
* [ItBlockarrayComAcceptQuoteController](#it_blockarray_com_accept_quote_controller)

## <a name="system_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.SystemController") SystemController

### Get singleton instance

The singleton instance of the ``` SystemController ``` class can be accessed from the API Client.

```csharp
SystemController system = client.System;
```

### <a name="get_system_ping"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.GetSystemPing") GetSystemPing

> *Tags:*  ``` Skips Authentication ``` 

> Test the connection to the business network


```csharp
Task<Models.PingResponse> GetSystemPing()
```

#### Example Usage

```csharp

Models.PingResponse result = await system.GetSystemPing();

```


### <a name="get_system_get_all_identities"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.GetSystemGetAllIdentities") GetSystemGetAllIdentities

> *Tags:*  ``` Skips Authentication ``` 

> Get all identities from the identity registry


```csharp
Task<dynamic> GetSystemGetAllIdentities()
```

#### Example Usage

```csharp

dynamic result = await system.GetSystemGetAllIdentities();

```


### <a name="get_system_get_identity_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.GetSystemGetIdentityByID") GetSystemGetIdentityByID

> *Tags:*  ``` Skips Authentication ``` 

> Get the specified identity from the identity registry


```csharp
Task<dynamic> GetSystemGetIdentityByID(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string id = "id";

dynamic result = await system.GetSystemGetIdentityByID(id);

```


### <a name="create_system_issue_identity"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.CreateSystemIssueIdentity") CreateSystemIssueIdentity

> *Tags:*  ``` Skips Authentication ``` 

> Issue an identity to the specified participant


```csharp
Task<Stream> CreateSystemIssueIdentity(Models.IssueIdentityRequest data)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var data = new Models.IssueIdentityRequest();

Stream result = await system.CreateSystemIssueIdentity(data);

```


### <a name="create_system_bind_identity"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.CreateSystemBindIdentity") CreateSystemBindIdentity

> *Tags:*  ``` Skips Authentication ``` 

> Bind an identity to the specified participant


```csharp
Task CreateSystemBindIdentity(Models.BindIdentityRequest data)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var data = new Models.BindIdentityRequest();

await system.CreateSystemBindIdentity(data);

```


### <a name="create_system_revoke_identity"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.CreateSystemRevokeIdentity") CreateSystemRevokeIdentity

> *Tags:*  ``` Skips Authentication ``` 

> Revoke the specified identity


```csharp
Task CreateSystemRevokeIdentity(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string id = "id";

await system.CreateSystemRevokeIdentity(id);

```


### <a name="get_system_get_all_historian_records"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.GetSystemGetAllHistorianRecords") GetSystemGetAllHistorianRecords

> *Tags:*  ``` Skips Authentication ``` 

> Get all Historian Records from the Historian


```csharp
Task<dynamic> GetSystemGetAllHistorianRecords()
```

#### Example Usage

```csharp

dynamic result = await system.GetSystemGetAllHistorianRecords();

```


### <a name="get_system_get_historian_record_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.SystemController.GetSystemGetHistorianRecordByID") GetSystemGetHistorianRecordByID

> *Tags:*  ``` Skips Authentication ``` 

> Get the specified Historian Record from the Historian


```csharp
Task<dynamic> GetSystemGetHistorianRecordByID(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string id = "id";

dynamic result = await system.GetSystemGetHistorianRecordByID(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_driver_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverController") ItBlockarrayComDriverController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComDriverController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComDriverController itBlockarrayComDriver = client.ItBlockarrayComDriver;
```

### <a name="get_it_blockarray_com_driver_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverController.GetItBlockarrayComDriverFind") GetItBlockarrayComDriverFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComDriver>> GetItBlockarrayComDriverFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComDriver> result = await itBlockarrayComDriver.GetItBlockarrayComDriverFind(filter);

```


### <a name="create_it_blockarray_com_driver_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverController.CreateItBlockarrayComDriverCreate") CreateItBlockarrayComDriverCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDriver> CreateItBlockarrayComDriverCreate(Models.ItBlockarrayComDriver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComDriver();

Models.ItBlockarrayComDriver result = await itBlockarrayComDriver.CreateItBlockarrayComDriverCreate(data);

```


### <a name="get_it_blockarray_com_driver_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverController.GetItBlockarrayComDriverFindById") GetItBlockarrayComDriverFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComDriver> GetItBlockarrayComDriverFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComDriver result = await itBlockarrayComDriver.GetItBlockarrayComDriverFindById(id, filter);

```


### <a name="update_it_blockarray_com_driver_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverController.UpdateItBlockarrayComDriverReplaceById") UpdateItBlockarrayComDriverReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDriver> UpdateItBlockarrayComDriverReplaceById(string id, Models.ItBlockarrayComDriver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComDriver();

Models.ItBlockarrayComDriver result = await itBlockarrayComDriver.UpdateItBlockarrayComDriverReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_driver_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverController.DeleteItBlockarrayComDriverDeleteById") DeleteItBlockarrayComDriverDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComDriverDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComDriver.DeleteItBlockarrayComDriverDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_shipper_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComShipperController") ItBlockarrayComShipperController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComShipperController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComShipperController itBlockarrayComShipper = client.ItBlockarrayComShipper;
```

### <a name="get_it_blockarray_com_shipper_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComShipperController.GetItBlockarrayComShipperFind") GetItBlockarrayComShipperFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComShipper>> GetItBlockarrayComShipperFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComShipper> result = await itBlockarrayComShipper.GetItBlockarrayComShipperFind(filter);

```


### <a name="create_it_blockarray_com_shipper_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComShipperController.CreateItBlockarrayComShipperCreate") CreateItBlockarrayComShipperCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComShipper> CreateItBlockarrayComShipperCreate(Models.ItBlockarrayComShipper data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComShipper();

Models.ItBlockarrayComShipper result = await itBlockarrayComShipper.CreateItBlockarrayComShipperCreate(data);

```


### <a name="get_it_blockarray_com_shipper_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComShipperController.GetItBlockarrayComShipperFindById") GetItBlockarrayComShipperFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComShipper> GetItBlockarrayComShipperFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComShipper result = await itBlockarrayComShipper.GetItBlockarrayComShipperFindById(id, filter);

```


### <a name="update_it_blockarray_com_shipper_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComShipperController.UpdateItBlockarrayComShipperReplaceById") UpdateItBlockarrayComShipperReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComShipper> UpdateItBlockarrayComShipperReplaceById(string id, Models.ItBlockarrayComShipper data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComShipper();

Models.ItBlockarrayComShipper result = await itBlockarrayComShipper.UpdateItBlockarrayComShipperReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_shipper_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComShipperController.DeleteItBlockarrayComShipperDeleteById") DeleteItBlockarrayComShipperDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComShipperDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComShipper.DeleteItBlockarrayComShipperDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_carrier_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCarrierController") ItBlockarrayComCarrierController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComCarrierController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComCarrierController itBlockarrayComCarrier = client.ItBlockarrayComCarrier;
```

### <a name="get_it_blockarray_com_carrier_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCarrierController.GetItBlockarrayComCarrierFind") GetItBlockarrayComCarrierFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComCarrier>> GetItBlockarrayComCarrierFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComCarrier> result = await itBlockarrayComCarrier.GetItBlockarrayComCarrierFind(filter);

```


### <a name="create_it_blockarray_com_carrier_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCarrierController.CreateItBlockarrayComCarrierCreate") CreateItBlockarrayComCarrierCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComCarrier> CreateItBlockarrayComCarrierCreate(Models.ItBlockarrayComCarrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComCarrier();

Models.ItBlockarrayComCarrier result = await itBlockarrayComCarrier.CreateItBlockarrayComCarrierCreate(data);

```


### <a name="get_it_blockarray_com_carrier_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCarrierController.GetItBlockarrayComCarrierFindById") GetItBlockarrayComCarrierFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComCarrier> GetItBlockarrayComCarrierFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComCarrier result = await itBlockarrayComCarrier.GetItBlockarrayComCarrierFindById(id, filter);

```


### <a name="update_it_blockarray_com_carrier_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCarrierController.UpdateItBlockarrayComCarrierReplaceById") UpdateItBlockarrayComCarrierReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComCarrier> UpdateItBlockarrayComCarrierReplaceById(string id, Models.ItBlockarrayComCarrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComCarrier();

Models.ItBlockarrayComCarrier result = await itBlockarrayComCarrier.UpdateItBlockarrayComCarrierReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_carrier_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCarrierController.DeleteItBlockarrayComCarrierDeleteById") DeleteItBlockarrayComCarrierDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComCarrierDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComCarrier.DeleteItBlockarrayComCarrierDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_receiver_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComReceiverController") ItBlockarrayComReceiverController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComReceiverController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComReceiverController itBlockarrayComReceiver = client.ItBlockarrayComReceiver;
```

### <a name="get_it_blockarray_com_receiver_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComReceiverController.GetItBlockarrayComReceiverFind") GetItBlockarrayComReceiverFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComReceiver>> GetItBlockarrayComReceiverFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComReceiver> result = await itBlockarrayComReceiver.GetItBlockarrayComReceiverFind(filter);

```


### <a name="create_it_blockarray_com_receiver_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComReceiverController.CreateItBlockarrayComReceiverCreate") CreateItBlockarrayComReceiverCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComReceiver> CreateItBlockarrayComReceiverCreate(Models.ItBlockarrayComReceiver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComReceiver();

Models.ItBlockarrayComReceiver result = await itBlockarrayComReceiver.CreateItBlockarrayComReceiverCreate(data);

```


### <a name="get_it_blockarray_com_receiver_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComReceiverController.GetItBlockarrayComReceiverFindById") GetItBlockarrayComReceiverFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComReceiver> GetItBlockarrayComReceiverFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComReceiver result = await itBlockarrayComReceiver.GetItBlockarrayComReceiverFindById(id, filter);

```


### <a name="update_it_blockarray_com_receiver_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComReceiverController.UpdateItBlockarrayComReceiverReplaceById") UpdateItBlockarrayComReceiverReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComReceiver> UpdateItBlockarrayComReceiverReplaceById(string id, Models.ItBlockarrayComReceiver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComReceiver();

Models.ItBlockarrayComReceiver result = await itBlockarrayComReceiver.UpdateItBlockarrayComReceiverReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_receiver_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComReceiverController.DeleteItBlockarrayComReceiverDeleteById") DeleteItBlockarrayComReceiverDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComReceiverDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComReceiver.DeleteItBlockarrayComReceiverDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_driver_passport_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverPassportController") ItBlockarrayComDriverPassportController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComDriverPassportController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComDriverPassportController itBlockarrayComDriverPassport = client.ItBlockarrayComDriverPassport;
```

### <a name="get_it_blockarray_com_driver_passport_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverPassportController.GetItBlockarrayComDriverPassportFind") GetItBlockarrayComDriverPassportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComDriverPassport>> GetItBlockarrayComDriverPassportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComDriverPassport> result = await itBlockarrayComDriverPassport.GetItBlockarrayComDriverPassportFind(filter);

```


### <a name="create_it_blockarray_com_driver_passport_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverPassportController.CreateItBlockarrayComDriverPassportCreate") CreateItBlockarrayComDriverPassportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDriverPassport> CreateItBlockarrayComDriverPassportCreate(Models.ItBlockarrayComDriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComDriverPassport();

Models.ItBlockarrayComDriverPassport result = await itBlockarrayComDriverPassport.CreateItBlockarrayComDriverPassportCreate(data);

```


### <a name="get_it_blockarray_com_driver_passport_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverPassportController.GetItBlockarrayComDriverPassportFindById") GetItBlockarrayComDriverPassportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComDriverPassport> GetItBlockarrayComDriverPassportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComDriverPassport result = await itBlockarrayComDriverPassport.GetItBlockarrayComDriverPassportFindById(id, filter);

```


### <a name="update_it_blockarray_com_driver_passport_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverPassportController.UpdateItBlockarrayComDriverPassportReplaceById") UpdateItBlockarrayComDriverPassportReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDriverPassport> UpdateItBlockarrayComDriverPassportReplaceById(string id, Models.ItBlockarrayComDriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComDriverPassport();

Models.ItBlockarrayComDriverPassport result = await itBlockarrayComDriverPassport.UpdateItBlockarrayComDriverPassportReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_driver_passport_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDriverPassportController.DeleteItBlockarrayComDriverPassportDeleteById") DeleteItBlockarrayComDriverPassportDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComDriverPassportDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComDriverPassport.DeleteItBlockarrayComDriverPassportDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_add_driver_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAddDriverController") ItBlockarrayComAddDriverController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComAddDriverController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComAddDriverController itBlockarrayComAddDriver = client.ItBlockarrayComAddDriver;
```

### <a name="get_it_blockarray_com_add_driver_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAddDriverController.GetItBlockarrayComAddDriverFind") GetItBlockarrayComAddDriverFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComAddDriver>> GetItBlockarrayComAddDriverFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComAddDriver> result = await itBlockarrayComAddDriver.GetItBlockarrayComAddDriverFind(filter);

```


### <a name="create_it_blockarray_com_add_driver_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAddDriverController.CreateItBlockarrayComAddDriverCreate") CreateItBlockarrayComAddDriverCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComAddDriver> CreateItBlockarrayComAddDriverCreate(Models.ItBlockarrayComAddDriver data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComAddDriver();

Models.ItBlockarrayComAddDriver result = await itBlockarrayComAddDriver.CreateItBlockarrayComAddDriverCreate(data);

```


### <a name="get_it_blockarray_com_add_driver_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAddDriverController.GetItBlockarrayComAddDriverFindById") GetItBlockarrayComAddDriverFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComAddDriver> GetItBlockarrayComAddDriverFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComAddDriver result = await itBlockarrayComAddDriver.GetItBlockarrayComAddDriverFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_create_driver_passport_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCreateDriverPassportController") ItBlockarrayComCreateDriverPassportController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComCreateDriverPassportController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComCreateDriverPassportController itBlockarrayComCreateDriverPassport = client.ItBlockarrayComCreateDriverPassport;
```

### <a name="get_it_blockarray_com_create_driver_passport_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCreateDriverPassportController.GetItBlockarrayComCreateDriverPassportFind") GetItBlockarrayComCreateDriverPassportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComCreateDriverPassport>> GetItBlockarrayComCreateDriverPassportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComCreateDriverPassport> result = await itBlockarrayComCreateDriverPassport.GetItBlockarrayComCreateDriverPassportFind(filter);

```


### <a name="create_it_blockarray_com_create_driver_passport_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCreateDriverPassportController.CreateItBlockarrayComCreateDriverPassportCreate") CreateItBlockarrayComCreateDriverPassportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComCreateDriverPassport> CreateItBlockarrayComCreateDriverPassportCreate(Models.ItBlockarrayComCreateDriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComCreateDriverPassport();

Models.ItBlockarrayComCreateDriverPassport result = await itBlockarrayComCreateDriverPassport.CreateItBlockarrayComCreateDriverPassportCreate(data);

```


### <a name="get_it_blockarray_com_create_driver_passport_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComCreateDriverPassportController.GetItBlockarrayComCreateDriverPassportFindById") GetItBlockarrayComCreateDriverPassportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComCreateDriverPassport> GetItBlockarrayComCreateDriverPassportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComCreateDriverPassport result = await itBlockarrayComCreateDriverPassport.GetItBlockarrayComCreateDriverPassportFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_update_driver_passport_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComUpdateDriverPassportController") ItBlockarrayComUpdateDriverPassportController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComUpdateDriverPassportController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComUpdateDriverPassportController itBlockarrayComUpdateDriverPassport = client.ItBlockarrayComUpdateDriverPassport;
```

### <a name="get_it_blockarray_com_update_driver_passport_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComUpdateDriverPassportController.GetItBlockarrayComUpdateDriverPassportFind") GetItBlockarrayComUpdateDriverPassportFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComUpdateDriverPassport>> GetItBlockarrayComUpdateDriverPassportFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComUpdateDriverPassport> result = await itBlockarrayComUpdateDriverPassport.GetItBlockarrayComUpdateDriverPassportFind(filter);

```


### <a name="create_it_blockarray_com_update_driver_passport_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComUpdateDriverPassportController.CreateItBlockarrayComUpdateDriverPassportCreate") CreateItBlockarrayComUpdateDriverPassportCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComUpdateDriverPassport> CreateItBlockarrayComUpdateDriverPassportCreate(Models.ItBlockarrayComUpdateDriverPassport data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComUpdateDriverPassport();

Models.ItBlockarrayComUpdateDriverPassport result = await itBlockarrayComUpdateDriverPassport.CreateItBlockarrayComUpdateDriverPassportCreate(data);

```


### <a name="get_it_blockarray_com_update_driver_passport_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComUpdateDriverPassportController.GetItBlockarrayComUpdateDriverPassportFindById") GetItBlockarrayComUpdateDriverPassportFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComUpdateDriverPassport> GetItBlockarrayComUpdateDriverPassportFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComUpdateDriverPassport result = await itBlockarrayComUpdateDriverPassport.GetItBlockarrayComUpdateDriverPassportFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_change_driver_carrier_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComChangeDriverCarrierController") ItBlockarrayComChangeDriverCarrierController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComChangeDriverCarrierController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComChangeDriverCarrierController itBlockarrayComChangeDriverCarrier = client.ItBlockarrayComChangeDriverCarrier;
```

### <a name="get_it_blockarray_com_change_driver_carrier_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComChangeDriverCarrierController.GetItBlockarrayComChangeDriverCarrierFind") GetItBlockarrayComChangeDriverCarrierFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComChangeDriverCarrier>> GetItBlockarrayComChangeDriverCarrierFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComChangeDriverCarrier> result = await itBlockarrayComChangeDriverCarrier.GetItBlockarrayComChangeDriverCarrierFind(filter);

```


### <a name="create_it_blockarray_com_change_driver_carrier_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComChangeDriverCarrierController.CreateItBlockarrayComChangeDriverCarrierCreate") CreateItBlockarrayComChangeDriverCarrierCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComChangeDriverCarrier> CreateItBlockarrayComChangeDriverCarrierCreate(Models.ItBlockarrayComChangeDriverCarrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComChangeDriverCarrier();

Models.ItBlockarrayComChangeDriverCarrier result = await itBlockarrayComChangeDriverCarrier.CreateItBlockarrayComChangeDriverCarrierCreate(data);

```


### <a name="get_it_blockarray_com_change_driver_carrier_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComChangeDriverCarrierController.GetItBlockarrayComChangeDriverCarrierFindById") GetItBlockarrayComChangeDriverCarrierFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComChangeDriverCarrier> GetItBlockarrayComChangeDriverCarrierFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComChangeDriverCarrier result = await itBlockarrayComChangeDriverCarrier.GetItBlockarrayComChangeDriverCarrierFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_remove_driver_carrier_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComRemoveDriverCarrierController") ItBlockarrayComRemoveDriverCarrierController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComRemoveDriverCarrierController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComRemoveDriverCarrierController itBlockarrayComRemoveDriverCarrier = client.ItBlockarrayComRemoveDriverCarrier;
```

### <a name="get_it_blockarray_com_remove_driver_carrier_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComRemoveDriverCarrierController.GetItBlockarrayComRemoveDriverCarrierFind") GetItBlockarrayComRemoveDriverCarrierFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComRemoveDriverCarrier>> GetItBlockarrayComRemoveDriverCarrierFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComRemoveDriverCarrier> result = await itBlockarrayComRemoveDriverCarrier.GetItBlockarrayComRemoveDriverCarrierFind(filter);

```


### <a name="create_it_blockarray_com_remove_driver_carrier_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComRemoveDriverCarrierController.CreateItBlockarrayComRemoveDriverCarrierCreate") CreateItBlockarrayComRemoveDriverCarrierCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComRemoveDriverCarrier> CreateItBlockarrayComRemoveDriverCarrierCreate(Models.ItBlockarrayComRemoveDriverCarrier data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComRemoveDriverCarrier();

Models.ItBlockarrayComRemoveDriverCarrier result = await itBlockarrayComRemoveDriverCarrier.CreateItBlockarrayComRemoveDriverCarrierCreate(data);

```


### <a name="get_it_blockarray_com_remove_driver_carrier_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComRemoveDriverCarrierController.GetItBlockarrayComRemoveDriverCarrierFindById") GetItBlockarrayComRemoveDriverCarrierFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComRemoveDriverCarrier> GetItBlockarrayComRemoveDriverCarrierFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComRemoveDriverCarrier result = await itBlockarrayComRemoveDriverCarrier.GetItBlockarrayComRemoveDriverCarrierFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_detention_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDetentionController") ItBlockarrayComDetentionController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComDetentionController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComDetentionController itBlockarrayComDetention = client.ItBlockarrayComDetention;
```

### <a name="get_it_blockarray_com_detention_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDetentionController.GetItBlockarrayComDetentionFind") GetItBlockarrayComDetentionFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComDetention>> GetItBlockarrayComDetentionFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComDetention> result = await itBlockarrayComDetention.GetItBlockarrayComDetentionFind(filter);

```


### <a name="create_it_blockarray_com_detention_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDetentionController.CreateItBlockarrayComDetentionCreate") CreateItBlockarrayComDetentionCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDetention> CreateItBlockarrayComDetentionCreate(Models.ItBlockarrayComDetention data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComDetention();

Models.ItBlockarrayComDetention result = await itBlockarrayComDetention.CreateItBlockarrayComDetentionCreate(data);

```


### <a name="get_it_blockarray_com_detention_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDetentionController.GetItBlockarrayComDetentionFindById") GetItBlockarrayComDetentionFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComDetention> GetItBlockarrayComDetentionFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComDetention result = await itBlockarrayComDetention.GetItBlockarrayComDetentionFindById(id, filter);

```


### <a name="update_it_blockarray_com_detention_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDetentionController.UpdateItBlockarrayComDetentionReplaceById") UpdateItBlockarrayComDetentionReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDetention> UpdateItBlockarrayComDetentionReplaceById(string id, Models.ItBlockarrayComDetention data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComDetention();

Models.ItBlockarrayComDetention result = await itBlockarrayComDetention.UpdateItBlockarrayComDetentionReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_detention_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDetentionController.DeleteItBlockarrayComDetentionDeleteById") DeleteItBlockarrayComDetentionDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComDetentionDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComDetention.DeleteItBlockarrayComDetentionDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_quote_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComQuoteController") ItBlockarrayComQuoteController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComQuoteController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComQuoteController itBlockarrayComQuote = client.ItBlockarrayComQuote;
```

### <a name="get_it_blockarray_com_quote_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComQuoteController.GetItBlockarrayComQuoteFind") GetItBlockarrayComQuoteFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComQuote>> GetItBlockarrayComQuoteFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComQuote> result = await itBlockarrayComQuote.GetItBlockarrayComQuoteFind(filter);

```


### <a name="create_it_blockarray_com_quote_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComQuoteController.CreateItBlockarrayComQuoteCreate") CreateItBlockarrayComQuoteCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComQuote> CreateItBlockarrayComQuoteCreate(Models.ItBlockarrayComQuote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComQuote();

Models.ItBlockarrayComQuote result = await itBlockarrayComQuote.CreateItBlockarrayComQuoteCreate(data);

```


### <a name="get_it_blockarray_com_quote_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComQuoteController.GetItBlockarrayComQuoteFindById") GetItBlockarrayComQuoteFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComQuote> GetItBlockarrayComQuoteFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComQuote result = await itBlockarrayComQuote.GetItBlockarrayComQuoteFindById(id, filter);

```


### <a name="update_it_blockarray_com_quote_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComQuoteController.UpdateItBlockarrayComQuoteReplaceById") UpdateItBlockarrayComQuoteReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComQuote> UpdateItBlockarrayComQuoteReplaceById(string id, Models.ItBlockarrayComQuote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComQuote();

Models.ItBlockarrayComQuote result = await itBlockarrayComQuote.UpdateItBlockarrayComQuoteReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_quote_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComQuoteController.DeleteItBlockarrayComQuoteDeleteById") DeleteItBlockarrayComQuoteDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComQuoteDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComQuote.DeleteItBlockarrayComQuoteDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_load_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadController") ItBlockarrayComLoadController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComLoadController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComLoadController itBlockarrayComLoad = client.ItBlockarrayComLoad;
```

### <a name="get_it_blockarray_com_load_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadController.GetItBlockarrayComLoadFind") GetItBlockarrayComLoadFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComLoad>> GetItBlockarrayComLoadFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComLoad> result = await itBlockarrayComLoad.GetItBlockarrayComLoadFind(filter);

```


### <a name="create_it_blockarray_com_load_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadController.CreateItBlockarrayComLoadCreate") CreateItBlockarrayComLoadCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComLoad> CreateItBlockarrayComLoadCreate(Models.ItBlockarrayComLoad data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComLoad();

Models.ItBlockarrayComLoad result = await itBlockarrayComLoad.CreateItBlockarrayComLoadCreate(data);

```


### <a name="get_it_blockarray_com_load_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadController.GetItBlockarrayComLoadFindById") GetItBlockarrayComLoadFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComLoad> GetItBlockarrayComLoadFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComLoad result = await itBlockarrayComLoad.GetItBlockarrayComLoadFindById(id, filter);

```


### <a name="update_it_blockarray_com_load_replace_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadController.UpdateItBlockarrayComLoadReplaceById") UpdateItBlockarrayComLoadReplaceById

> *Tags:*  ``` Skips Authentication ``` 

> Replace attributes for a model instance and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComLoad> UpdateItBlockarrayComLoadReplaceById(string id, Models.ItBlockarrayComLoad data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
string id = "id";
var data = new Models.ItBlockarrayComLoad();

Models.ItBlockarrayComLoad result = await itBlockarrayComLoad.UpdateItBlockarrayComLoadReplaceById(id, data);

```


### <a name="delete_it_blockarray_com_load_delete_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadController.DeleteItBlockarrayComLoadDeleteById") DeleteItBlockarrayComLoadDeleteById

> *Tags:*  ``` Skips Authentication ``` 

> Delete a model instance by {{id}} from the data source.


```csharp
Task<dynamic> DeleteItBlockarrayComLoadDeleteById(string id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |


#### Example Usage

```csharp
string id = "id";

dynamic result = await itBlockarrayComLoad.DeleteItBlockarrayComLoadDeleteById(id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_assign_driver_to_load_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAssignDriverToLoadController") ItBlockarrayComAssignDriverToLoadController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComAssignDriverToLoadController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComAssignDriverToLoadController itBlockarrayComAssignDriverToLoad = client.ItBlockarrayComAssignDriverToLoad;
```

### <a name="get_it_blockarray_com_assign_driver_to_load_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAssignDriverToLoadController.GetItBlockarrayComAssignDriverToLoadFind") GetItBlockarrayComAssignDriverToLoadFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComAssignDriverToLoad>> GetItBlockarrayComAssignDriverToLoadFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComAssignDriverToLoad> result = await itBlockarrayComAssignDriverToLoad.GetItBlockarrayComAssignDriverToLoadFind(filter);

```


### <a name="create_it_blockarray_com_assign_driver_to_load_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAssignDriverToLoadController.CreateItBlockarrayComAssignDriverToLoadCreate") CreateItBlockarrayComAssignDriverToLoadCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComAssignDriverToLoad> CreateItBlockarrayComAssignDriverToLoadCreate(Models.ItBlockarrayComAssignDriverToLoad data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComAssignDriverToLoad();

Models.ItBlockarrayComAssignDriverToLoad result = await itBlockarrayComAssignDriverToLoad.CreateItBlockarrayComAssignDriverToLoadCreate(data);

```


### <a name="get_it_blockarray_com_assign_driver_to_load_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAssignDriverToLoadController.GetItBlockarrayComAssignDriverToLoadFindById") GetItBlockarrayComAssignDriverToLoadFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComAssignDriverToLoad> GetItBlockarrayComAssignDriverToLoadFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComAssignDriverToLoad result = await itBlockarrayComAssignDriverToLoad.GetItBlockarrayComAssignDriverToLoadFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_origin_arrival_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComOriginArrivalController") ItBlockarrayComOriginArrivalController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComOriginArrivalController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComOriginArrivalController itBlockarrayComOriginArrival = client.ItBlockarrayComOriginArrival;
```

### <a name="get_it_blockarray_com_origin_arrival_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComOriginArrivalController.GetItBlockarrayComOriginArrivalFind") GetItBlockarrayComOriginArrivalFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComOriginArrival>> GetItBlockarrayComOriginArrivalFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComOriginArrival> result = await itBlockarrayComOriginArrival.GetItBlockarrayComOriginArrivalFind(filter);

```


### <a name="create_it_blockarray_com_origin_arrival_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComOriginArrivalController.CreateItBlockarrayComOriginArrivalCreate") CreateItBlockarrayComOriginArrivalCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComOriginArrival> CreateItBlockarrayComOriginArrivalCreate(Models.ItBlockarrayComOriginArrival data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComOriginArrival();

Models.ItBlockarrayComOriginArrival result = await itBlockarrayComOriginArrival.CreateItBlockarrayComOriginArrivalCreate(data);

```


### <a name="get_it_blockarray_com_origin_arrival_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComOriginArrivalController.GetItBlockarrayComOriginArrivalFindById") GetItBlockarrayComOriginArrivalFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComOriginArrival> GetItBlockarrayComOriginArrivalFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComOriginArrival result = await itBlockarrayComOriginArrival.GetItBlockarrayComOriginArrivalFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_load_pickup_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadPickupController") ItBlockarrayComLoadPickupController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComLoadPickupController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComLoadPickupController itBlockarrayComLoadPickup = client.ItBlockarrayComLoadPickup;
```

### <a name="get_it_blockarray_com_load_pickup_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadPickupController.GetItBlockarrayComLoadPickupFind") GetItBlockarrayComLoadPickupFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComLoadPickup>> GetItBlockarrayComLoadPickupFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComLoadPickup> result = await itBlockarrayComLoadPickup.GetItBlockarrayComLoadPickupFind(filter);

```


### <a name="create_it_blockarray_com_load_pickup_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadPickupController.CreateItBlockarrayComLoadPickupCreate") CreateItBlockarrayComLoadPickupCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComLoadPickup> CreateItBlockarrayComLoadPickupCreate(Models.ItBlockarrayComLoadPickup data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComLoadPickup();

Models.ItBlockarrayComLoadPickup result = await itBlockarrayComLoadPickup.CreateItBlockarrayComLoadPickupCreate(data);

```


### <a name="get_it_blockarray_com_load_pickup_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadPickupController.GetItBlockarrayComLoadPickupFindById") GetItBlockarrayComLoadPickupFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComLoadPickup> GetItBlockarrayComLoadPickupFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComLoadPickup result = await itBlockarrayComLoadPickup.GetItBlockarrayComLoadPickupFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_destination_arrival_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDestinationArrivalController") ItBlockarrayComDestinationArrivalController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComDestinationArrivalController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComDestinationArrivalController itBlockarrayComDestinationArrival = client.ItBlockarrayComDestinationArrival;
```

### <a name="get_it_blockarray_com_destination_arrival_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDestinationArrivalController.GetItBlockarrayComDestinationArrivalFind") GetItBlockarrayComDestinationArrivalFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComDestinationArrival>> GetItBlockarrayComDestinationArrivalFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComDestinationArrival> result = await itBlockarrayComDestinationArrival.GetItBlockarrayComDestinationArrivalFind(filter);

```


### <a name="create_it_blockarray_com_destination_arrival_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDestinationArrivalController.CreateItBlockarrayComDestinationArrivalCreate") CreateItBlockarrayComDestinationArrivalCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComDestinationArrival> CreateItBlockarrayComDestinationArrivalCreate(Models.ItBlockarrayComDestinationArrival data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComDestinationArrival();

Models.ItBlockarrayComDestinationArrival result = await itBlockarrayComDestinationArrival.CreateItBlockarrayComDestinationArrivalCreate(data);

```


### <a name="get_it_blockarray_com_destination_arrival_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComDestinationArrivalController.GetItBlockarrayComDestinationArrivalFindById") GetItBlockarrayComDestinationArrivalFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComDestinationArrival> GetItBlockarrayComDestinationArrivalFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComDestinationArrival result = await itBlockarrayComDestinationArrival.GetItBlockarrayComDestinationArrivalFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_load_drop_off_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadDropOffController") ItBlockarrayComLoadDropOffController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComLoadDropOffController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComLoadDropOffController itBlockarrayComLoadDropOff = client.ItBlockarrayComLoadDropOff;
```

### <a name="get_it_blockarray_com_load_drop_off_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadDropOffController.GetItBlockarrayComLoadDropOffFind") GetItBlockarrayComLoadDropOffFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComLoadDropOff>> GetItBlockarrayComLoadDropOffFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComLoadDropOff> result = await itBlockarrayComLoadDropOff.GetItBlockarrayComLoadDropOffFind(filter);

```


### <a name="create_it_blockarray_com_load_drop_off_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadDropOffController.CreateItBlockarrayComLoadDropOffCreate") CreateItBlockarrayComLoadDropOffCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComLoadDropOff> CreateItBlockarrayComLoadDropOffCreate(Models.ItBlockarrayComLoadDropOff data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComLoadDropOff();

Models.ItBlockarrayComLoadDropOff result = await itBlockarrayComLoadDropOff.CreateItBlockarrayComLoadDropOffCreate(data);

```


### <a name="get_it_blockarray_com_load_drop_off_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComLoadDropOffController.GetItBlockarrayComLoadDropOffFindById") GetItBlockarrayComLoadDropOffFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComLoadDropOff> GetItBlockarrayComLoadDropOffFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComLoadDropOff result = await itBlockarrayComLoadDropOff.GetItBlockarrayComLoadDropOffFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_list_load_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComListLoadController") ItBlockarrayComListLoadController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComListLoadController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComListLoadController itBlockarrayComListLoad = client.ItBlockarrayComListLoad;
```

### <a name="get_it_blockarray_com_list_load_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComListLoadController.GetItBlockarrayComListLoadFind") GetItBlockarrayComListLoadFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComListLoad>> GetItBlockarrayComListLoadFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComListLoad> result = await itBlockarrayComListLoad.GetItBlockarrayComListLoadFind(filter);

```


### <a name="create_it_blockarray_com_list_load_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComListLoadController.CreateItBlockarrayComListLoadCreate") CreateItBlockarrayComListLoadCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComListLoad> CreateItBlockarrayComListLoadCreate(Models.ItBlockarrayComListLoad data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComListLoad();

Models.ItBlockarrayComListLoad result = await itBlockarrayComListLoad.CreateItBlockarrayComListLoadCreate(data);

```


### <a name="get_it_blockarray_com_list_load_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComListLoadController.GetItBlockarrayComListLoadFindById") GetItBlockarrayComListLoadFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComListLoad> GetItBlockarrayComListLoadFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComListLoad result = await itBlockarrayComListLoad.GetItBlockarrayComListLoadFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_submit_quote_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComSubmitQuoteController") ItBlockarrayComSubmitQuoteController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComSubmitQuoteController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComSubmitQuoteController itBlockarrayComSubmitQuote = client.ItBlockarrayComSubmitQuote;
```

### <a name="get_it_blockarray_com_submit_quote_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComSubmitQuoteController.GetItBlockarrayComSubmitQuoteFind") GetItBlockarrayComSubmitQuoteFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComSubmitQuote>> GetItBlockarrayComSubmitQuoteFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComSubmitQuote> result = await itBlockarrayComSubmitQuote.GetItBlockarrayComSubmitQuoteFind(filter);

```


### <a name="create_it_blockarray_com_submit_quote_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComSubmitQuoteController.CreateItBlockarrayComSubmitQuoteCreate") CreateItBlockarrayComSubmitQuoteCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComSubmitQuote> CreateItBlockarrayComSubmitQuoteCreate(Models.ItBlockarrayComSubmitQuote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComSubmitQuote();

Models.ItBlockarrayComSubmitQuote result = await itBlockarrayComSubmitQuote.CreateItBlockarrayComSubmitQuoteCreate(data);

```


### <a name="get_it_blockarray_com_submit_quote_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComSubmitQuoteController.GetItBlockarrayComSubmitQuoteFindById") GetItBlockarrayComSubmitQuoteFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComSubmitQuote> GetItBlockarrayComSubmitQuoteFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComSubmitQuote result = await itBlockarrayComSubmitQuote.GetItBlockarrayComSubmitQuoteFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="it_blockarray_com_accept_quote_controller"></a>![Class: ](https://apidocs.io/img/class.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAcceptQuoteController") ItBlockarrayComAcceptQuoteController

### Get singleton instance

The singleton instance of the ``` ItBlockarrayComAcceptQuoteController ``` class can be accessed from the API Client.

```csharp
ItBlockarrayComAcceptQuoteController itBlockarrayComAcceptQuote = client.ItBlockarrayComAcceptQuote;
```

### <a name="get_it_blockarray_com_accept_quote_find"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAcceptQuoteController.GetItBlockarrayComAcceptQuoteFind") GetItBlockarrayComAcceptQuoteFind

> *Tags:*  ``` Skips Authentication ``` 

> Find all instances of the model matched by filter from the data source.


```csharp
Task<List<Models.ItBlockarrayComAcceptQuote>> GetItBlockarrayComAcceptQuoteFind(string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| filter |  ``` Optional ```  | Filter defining fields, where, include, order, offset, and limit - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string filter = "filter";

List<Models.ItBlockarrayComAcceptQuote> result = await itBlockarrayComAcceptQuote.GetItBlockarrayComAcceptQuoteFind(filter);

```


### <a name="create_it_blockarray_com_accept_quote_create"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAcceptQuoteController.CreateItBlockarrayComAcceptQuoteCreate") CreateItBlockarrayComAcceptQuoteCreate

> *Tags:*  ``` Skips Authentication ``` 

> Create a new instance of the model and persist it into the data source.


```csharp
Task<Models.ItBlockarrayComAcceptQuote> CreateItBlockarrayComAcceptQuoteCreate(Models.ItBlockarrayComAcceptQuote data = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Optional ```  | Model instance data |


#### Example Usage

```csharp
var data = new Models.ItBlockarrayComAcceptQuote();

Models.ItBlockarrayComAcceptQuote result = await itBlockarrayComAcceptQuote.CreateItBlockarrayComAcceptQuoteCreate(data);

```


### <a name="get_it_blockarray_com_accept_quote_find_by_id"></a>![Method: ](https://apidocs.io/img/method.png "BlockarrayNetwork.Standard.Controllers.ItBlockarrayComAcceptQuoteController.GetItBlockarrayComAcceptQuoteFindById") GetItBlockarrayComAcceptQuoteFindById

> *Tags:*  ``` Skips Authentication ``` 

> Find a model instance by {{id}} from the data source.


```csharp
Task<Models.ItBlockarrayComAcceptQuote> GetItBlockarrayComAcceptQuoteFindById(string id, string filter = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | Model id |
| filter |  ``` Optional ```  | Filter defining fields and include - must be a JSON-encoded string ({"something":"value"}) |


#### Example Usage

```csharp
string id = "id";
string filter = "filter";

Models.ItBlockarrayComAcceptQuote result = await itBlockarrayComAcceptQuote.GetItBlockarrayComAcceptQuoteFindById(id, filter);

```


[Back to List of Controllers](#list_of_controllers)



