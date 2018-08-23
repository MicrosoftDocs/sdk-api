---
UID: NN:msclus.ISClusProperties
title: ISClusProperties
author: windows-sdk-content
description: Provides access to the properties of a cluster object, allowing individual property values to be changed.
old-location: mscs\clusproperties_collection.htm
old-project: mscs
ms.assetid: b117b0eb-e188-4514-8e11-9acca1303e8f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusProperties, ClusProperties collection [Failover Cluster], ClusProperties collection [Failover Cluster],described, ISClusProperties, _wolf_clusproperties_collection, msclus/ClusProperties, mscs.clusproperties_collection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusProperties
 - ISClusProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperties interface


## -description


<p class="CCE_Message">[The 
    <b>ClusProperties</b> collection is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Provides access to the properties of a 
    <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>, allowing individual property values to be 
    changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusProperties</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusProperties</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8df57999-5866-4005-9825-fefb827c876d">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> object and adds it 
     to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">Refresh</a>
</td>
<td align="left" width="63%">
Updates the collection with current property data from the 
     <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">SaveChanges</a>
</td>
<td align="left" width="63%">
Saves all property data in the collection to the cluster database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ac19293-d489-41ee-b585-6997a29591af">UseDefaultValue</a>
</td>
<td align="left" width="63%">
Deletes a property from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusProperties</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7003b7e6-56f9-4499-9967-966ba23c40ed">Common</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the properties in the collection are 
     <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6988a8c6-b1ef-4dba-b95c-eab52f140fb3">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the number of properties in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/df848e91-c89d-4985-9afc-1814f3180283">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a single property from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5eaeffda-e2ce-420a-b3f5-da8dfbfdde24">Modified</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether any properties in the collection have been added, removed, or modified since the last 
     <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">Refresh</a> or 
     <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">SaveChanges</a> operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/94ce9052-98af-4edd-b3da-6aeff40d8242">Private</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the properties in the collection are 
     <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/879bd8a6-3203-4ff0-8277-88c92ea8dbf3">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the properties in the collection are 
     <a href="https://msdn.microsoft.com/7df0981b-7253-40c1-9a5d-44cfc4cdf13b">read-only properties</a>.

</td>
</tr>
</table> 


## -remarks



A <b>ClusProperties</b> collection is similar 
    to a <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> in that the data in the collection is a 
    local copy of real data stored in the cluster database. When an instance of the 
    <b>ClusProperties</b> collection is created, it 
    receives a snapshot of the stored data. Changes to the 
    <b>ClusProperties</b> collection do not take 
    effect in the <a href="c_gly.htm">cluster</a> until the 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">SaveChanges</a> method is invoked. Similarly, 
    changes to the cluster database are not reflected in the collection until the 
    <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">Refresh</a> method is called.

A <b>ClusProperties</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> objects.</li>
<li>
Can be obtained from any of the following objects.


<a href="https://msdn.microsoft.com/d51e9872-eb86-4b0e-b417-1a2e5ac6ee9c">ClusNetwork</a>



<a href="https://msdn.microsoft.com/21aaf37d-5b60-4005-9e7f-f0435de590b2">ClusNetInterface</a>



<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a>


</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

