---
UID: NN:msclus.ISClusResTypeResources
title: ISClusResTypeResources
author: windows-sdk-content
description: Provides access to the resources of a particular type in a cluster.
old-location: mscs\clusrestyperesources_collection.htm
old-project: MsCS
ms.assetid: 3164f2ee-7230-4d77-8c7c-cfba3aaee9d4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusResTypeResources, ClusResTypeResources collection [Failover Cluster], ClusResTypeResources collection [Failover Cluster],described, ISClusResTypeResources, _wolf_clusrestyperesources_collection, msclus/ClusResTypeResources, mscs.clusrestyperesources_collection
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusResTypeResources
-	ISClusResTypeResources
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResTypeResources interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResTypeResources</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> of a particular 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">type</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResTypeResources</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResTypeResources</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/215482f4-4357-462b-bf67-109cc36e22b7">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new cluster resource and adds it to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be221cf6-0f27-48b2-bb87-5c7200841cd7">DeleteItem</a>
</td>
<td align="left" width="63%">
Deletes a resource from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6f9c220-824d-4d8b-bb2c-61b31ea7c52a">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResTypeResources</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Returns the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Returns a single resource from the collection.

</td>
</tr>
</table> 


## -remarks



A <a href="https://msdn.microsoft.com/a3269288-f32f-45d5-8fd4-4e6fb257c1be">ClusResPossibleOwnerNodes</a> 
    collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/2fa27a3c-c340-478a-af05-1583efb420b4">ClusResType.Resources</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/91aece2b-c47c-4e62-9aac-d546977d4848">Resource Type Management Objects</a>
 

 

