---
UID: NN:msclus.ISClusResGroup
title: ISClusResGroup
author: windows-sdk-content
description: Enables operations on a group, its properties, and related objects.
old-location: mscs\clusresgroup_object.htm
old-project: mscs
ms.assetid: cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusResGroup, ClusResGroup object [Failover Cluster], ClusResGroup object [Failover Cluster],described, ISClusResGroup, _wolf_clusresgroup_object, msclus/ClusResGroup, mscs.clusresgroup_object
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
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusResGroup
 - ISClusResGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroup interface


## -description


<p class="CCE_Message">[The <b>ClusResGroup</b> object 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Enables operations 
    on a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>, its properties, and related objects. Use 
    <b>ClusResGroup</b> to move groups between 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a>, bring groups 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">online</a> and 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">offline</a>, access the 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in the group, and perform other group-related tasks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroup</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResGroup</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1831340-67b9-458c-8669-c8e5e4973c28">Delete</a>
</td>
<td align="left" width="63%">
Deletes a group from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f923a22-31b2-4a41-b88d-8eb7bac9725e">Move</a>
</td>
<td align="left" width="63%">
Moves a group to the most preferred possible node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>
</td>
<td align="left" width="63%">
Takes a group offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
</td>
<td align="left" width="63%">
Brings a group online.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroup</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> associated with a group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/08c280a6-96c5-4e40-be42-4c798684482f">CommonProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the group's read/write 
     <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90de1234-d55c-40c2-9616-cfb3f9230c41">CommonROProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the group's read-only common properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Read/write property that sets the name of a group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d42e2f2e-5a67-4e9e-9e54-34f514c0a8f2">OwnerNode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a group's node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5e2872a4-72db-4cd8-9fce-34c1bd701706">PreferredOwnerNodes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a 
     <a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a> 
     collection providing access to the nodes that belong in a group's 
     <a href="https://msdn.microsoft.com/library/ms682858(v=VS.85).aspx">preferred owner</a> list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/79988509-16fb-4d75-96fa-7659d1831c34">PrivateProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the group's read/write 
     <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/61a518b2-7792-4336-98ce-63de7ffe0e32">PrivateROProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the group's read-only private properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/891a2126-774d-43c6-bd27-6a0e9d943383">Resources</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a 
     <a href="https://msdn.microsoft.com/9ea90beb-86ae-4026-94bb-175e593da8fa">ClusResGroupResources</a> collection 
     providing access to the resources in a group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7eb8662c-a6ca-46e5-99ee-84e0dd6b0961">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the state of a group.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResGroup</b> object:

<ul>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/415eecde-4057-4efe-aeae-2066e4b6c46a">Group Management Objects</a>
 

 

