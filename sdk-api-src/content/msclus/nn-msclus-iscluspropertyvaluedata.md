---
UID: NN:msclus.ISClusPropertyValueData
title: ISClusPropertyValueData
author: windows-sdk-content
description: All of the data values associated with a property value.
old-location: mscs\cluspropertyvaluedata_collection.htm
old-project: MsCS
ms.assetid: d95a90f6-2a70-428b-aff3-3be9e9e66071
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusPropertyValueData, ClusPropertyValueData collection [Failover Cluster], ClusPropertyValueData collection [Failover Cluster],described, ISClusPropertyValueData, _wolf_cluspropertyvaluedata_collection, msclus/ClusPropertyValueData, mscs.cluspropertyvaluedata_collection
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
 - ClusPropertyValueData
 - ISClusPropertyValueData
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusPropertyValueData interface


## -description


<p class="CCE_Message">[The 
    <b>ClusPropertyValueData</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Contains all of the <a href="p_gly.htm">data values</a> 
    associated with a <i>property value</i>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusPropertyValueData</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusPropertyValueData</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75bd2145-aed5-4a8f-b1da-e8fdcb0a537a">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new data value and adds it to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44cabe30-13ec-4303-9534-ab76e3c951ac">RemoveItem</a>
</td>
<td align="left" width="63%">
Deletes a data value from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusPropertyValueData</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the number of data values in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a single data value from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusPropertyValueData</b> 
    collection:

<ul>
<li>Contains data values.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/5305541c-ad28-4bdc-92e6-519ba5ab21d5">ClusPropertyValue.Data</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

