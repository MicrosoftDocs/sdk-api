---
UID: NN:msclus.ISClusResType
title: ISClusResType
author: windows-sdk-content
description: Enables operations on a resource type, its properties, and related objects.
old-location: mscs\clusrestype_object.htm
old-project: MsCS
ms.assetid: e4ad6364-f318-47f9-a276-d99c91ffbbb5
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusResType, ClusResType object [Failover Cluster], ClusResType object [Failover Cluster],described, ISClusResType, _wolf_clusrestype_object, msclus/ClusResType, mscs.clusrestype_object
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
 - ClusResType
 - ISClusResType
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResType interface


## -description


<p class="CCE_Message">[The <b>ClusResType</b> object is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Enables operations on a 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>, its properties, and related objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResType</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResType</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc700541-793b-423b-bea6-ad04deddb16a">AvailableDisks</a>
</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/2823ccb2-5fb2-4e37-b842-340703165871">ClusDisks</a> collection 
     representing the <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disks</a> available to the resource 
     type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b71789a5-7e88-418e-acf4-f28f60b03e3a">Delete</a>
</td>
<td align="left" width="63%">
Deletes the resource type.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResType</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>


</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> associated with the resource 
     type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cbed3cb1-ff86-4a60-9707-3e501fce95c5">CommonProperties</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the resource type's read/write 
     <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7e7e8fdf-d50f-4af2-aaf8-c878feb8d66b">CommonROProperties</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the resource type's read-only 
     <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9437a940-bb61-4de1-9d4b-54876161e02c">PossibleOwnerNodes</a>


</td>
<td align="left" width="63%">
Returns a 
     <a href="https://msdn.microsoft.com/be22d5b1-8c61-40a5-883c-f49651ba623d">ClusResTypePossibleOwnerNodes</a> 
     collection containing the <a href="p_gly.htm">possible owner</a> <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> of the resource type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b991f9c5-f1cd-447b-8474-74225bc60f15">PrivateProperties</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the resource type's read/write 
     <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/83cdc77c-3199-4d01-b71d-8337fd8314a9">PrivateROProperties</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
     containing the resource type's read-only private properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2fa27a3c-c340-478a-af05-1583efb420b4">Resources</a>


</td>
<td align="left" width="63%">
Returns all resources of a given type that are present in the cluster.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResType</b> object:

<ul>
<li>Is obtained from <a href="https://msdn.microsoft.com/614d3ed6-255f-46ed-9354-7a73a21cac87">ClusResTypes</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/91aece2b-c47c-4e62-9aac-d546977d4848">Resource Type Management Objects</a>
 

 

