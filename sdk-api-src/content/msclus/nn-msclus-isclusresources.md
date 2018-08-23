---
UID: NN:msclus.ISClusResources
title: ISClusResources
author: windows-sdk-content
description: Provides access to the resources that belong to a cluster.
old-location: mscs\clusresources_collection.htm
old-project: mscs
ms.assetid: 56dd53e7-7e2e-481f-b343-da51c7c52553
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResources, ClusResources collection [Failover Cluster], ClusResources collection [Failover Cluster],described, ISClusResources, _wolf_clusresources_collection, msclus/ClusResources, mscs.clusresources_collection
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
 - ClusResources
 - ISClusResources
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResources interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResources</b> collection is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Provides access to the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> that belong to a 
    <a href="c_gly.htm">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResources</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResources</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ff2d33b-08aa-445b-930e-7fbe589f6269">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new resource and adds it to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/200783e7-a2e6-489f-8271-36b8b6496b8e">DeleteItem</a>
</td>
<td align="left" width="63%">
Deletes a resource from the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db828d6a-6037-4d42-a32a-d99add06da18">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResources</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6c9ff4bd-8474-4e88-b70e-bc9e661382ab">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4d28c219-a308-4e07-9521-a80066ec91e3">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a single resource from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResources</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> objects.</li>
<li>Is obtained from <a href="https://msdn.microsoft.com/fdfdd1de-fa4a-4bfb-80e1-15b2141d488b">Cluster.Resources</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

