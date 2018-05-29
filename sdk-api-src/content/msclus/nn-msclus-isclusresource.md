---
UID: NN:msclus.ISClusResource
title: ISClusResource
author: windows-sdk-content
description: Enables operations on a resource, its properties, and related objects.
old-location: mscs\clusresource_object.htm
old-project: MsCS
ms.assetid: c1b66495-c428-4ee4-94e2-263fd31f61ad
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusResource, ClusResource object [Failover Cluster], ClusResource object [Failover Cluster],described, ISClusResource, _wolf_clusresource_object, msclus/ClusResource, mscs.clusresource_object
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusResource
-	ISClusResource
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource interface


## -description


<p class="CCE_Message">[The <b>ClusResource</b> object is available for use in the 
    operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Enables operations on a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>, its properties, and related objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResource</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResource</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98727cb1-238f-4bd8-b83a-e3838f824a16">AddResourceNode</a>
</td>
<td align="left" width="63%">
Adds a new <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to the list of possible nodes that can host the 
      resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd316586-8553-4c4a-824e-ee5b7bf48184">BecomeQuorumResource</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d167192f-4577-49b6-aa1c-1dbd6d2aa98c">CanResourceBeDependent</a>
</td>
<td align="left" width="63%">
Determines if the resource can be <a href="d_gly.htm">dependent</a> on 
      another resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c272144f-f417-4ea5-8147-4f7bd02170b7">ChangeResourceGroup</a>
</td>
<td align="left" width="63%">
Moves the resource from its current <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> to a different 
      group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/051ea164-4d6e-49a7-a414-abf1c5cb3af5">Delete</a>
</td>
<td align="left" width="63%">
Deletes the resource from the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c184a7f3-b09a-4349-a940-20d622f729a6">Fail</a>
</td>
<td align="left" width="63%">
Initiates <a href="https://msdn.microsoft.com/library/windows/hardware/dn425147">failure</a> of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>
</td>
<td align="left" width="63%">
Takes the resource offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
</td>
<td align="left" width="63%">
Brings the resource online.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ec493da-4524-4015-8aa7-fb4a8c3d78de">RemoveResourceNode</a>
</td>
<td align="left" width="63%">
Removes a node from the list of possible nodes that can host the resource.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResource</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0af280ef-ea5a-4cca-8065-2ee74d2dafc1">ClassInfo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the resource class of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> that includes the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/14f80d93-541c-4893-8aa6-7b4ba90ecdea">CommonProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the resource's read/write 
      <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1ac3fc77-cfec-4f80-8f9f-7b1d8e9bc897">CommonROProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the resource's read-only common properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8e39aa2a-e24c-4d15-9fa9-dec3ecb472ea">CoreFlag</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns any  flags that  identify the resource as a <a href="https://msdn.microsoft.com/46b71882-be37-4c3f-a328-a394c1310958">core resource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/14f75dc0-6d6e-4b70-9481-d00132f2b87b">CryptoKeys</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/0078ba7a-24d7-4de6-af05-f1a03d9deb0a">ClusCryptoKeys</a> collection 
      containing the resource's <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">checkpointed</a> crypto keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/33539a29-1533-44fa-853d-9d4f1b3f1cca">Dependencies</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/10695840-38ec-4614-8bbd-5772a53dea4b">ClusResDependencies</a> 
      collection providing access to the resource's 
      <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/88206f61-9e90-4335-8a34-fc0e6d1ca208">Dependents</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a> collection providing access to the list of the resource's dependent resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915271">Disk</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
For <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources, returns a 
      <a href="https://msdn.microsoft.com/6433d55f-f97a-4027-ba2a-7102b4cf33ae">ClusDisk</a> object providing access to information about 
      the disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">Group</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the group to which the resource belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aa39b401-bf18-48c5-83bb-e192efe1ef41">MaintenanceMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Returns or sets maintenance mode for a disk resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

<a href="https://msdn.microsoft.com/4daf586d-75ea-408b-a66d-48692f77a4f2">Read/write property</a> that either retrieves or 
      modifies the name of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dea1d13b-8a79-4ac4-ac29-437c520965f1">OwnerNode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the node that is hosting the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/591b0508-f963-4c62-afb8-1c9224299cc0">PossibleOwnerNodes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the nodes that are members of the resource's 
      <a href="p_gly.htm">possible owners</a> list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/eca63b55-9101-40fb-b2b2-3fb68e707745">PrivateProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the resource's read/write 
      <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/88869f08-db47-4661-bd23-7fe0bb491fa3">PrivateROProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the resource's read-only private properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/18bb4cfb-cd96-4f43-9cf6-ab06c22d0abf">RegistryKeys</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a> 
      collection containing the resource's checkpointed registry keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3bae66a8-cc45-49e6-acea-c506623b25bc">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns information about the current state of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the resource type of the resource as a 
      <a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a3230fa1-67f9-43d5-b06a-03ffc2487a63">TypeName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the resource type name of the resource.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResource</b> object is obtained from the 
     following collections:

<ul>
<li>
<a href="https://msdn.microsoft.com/9ea90beb-86ae-4026-94bb-175e593da8fa">ClusResGroupResources</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10695840-38ec-4614-8bbd-5772a53dea4b">ClusResDependencies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3164f2ee-7230-4d77-8c7c-cfba3aaee9d4">ClusResTypeResources</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/fa3a5042-8bb5-4ece-825c-40d7df584b35">Resource Management Objects</a>
 

 

