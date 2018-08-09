---
UID: NN:msclus.ISClusPropertyValues
title: ISClusPropertyValues
author: windows-sdk-content
description: Contains all of the property values associated with a multi-value property, with each value represented by a ClusPropertyValue object.
old-location: mscs\cluspropertyvalues_collection.htm
old-project: mscs
ms.assetid: 18ae71ee-5582-4ac9-bb0f-f1c077c0352a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusPropertyValues, ClusPropertyValues collection [Failover Cluster], ClusPropertyValues collection [Failover Cluster],described, ISClusPropertyValues, _wolf_cluspropertyvalues_collection, msclus/ClusPropertyValues, mscs.cluspropertyvalues_collection
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
 - ClusPropertyValues
 - ISClusPropertyValues
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusPropertyValues interface


## -description


<p class="CCE_Message">[The 
    <b>ClusPropertyValues</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Contains all of the <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">property values</a> 
    associated with a multi-value property, with each value represented by a 
    <a href="https://msdn.microsoft.com/6a8ffae6-c4f3-42fb-9703-eeb695902877">ClusPropertyValue</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusPropertyValues</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusPropertyValues</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7175a46-3e0c-4d71-b435-589a145a56f3">CreateItem</a>
</td>
<td align="left" width="63%">
Adds a property value to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86184297-c7e1-41da-b760-fbda1ae949ae">RemoveItem</a>
</td>
<td align="left" width="63%">
Deletes a property value from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusPropertyValues</b> collection has these properties.
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
Returns the number of property values in the collection.

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
Returns a single property value from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusPropertyValues</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/6a8ffae6-c4f3-42fb-9703-eeb695902877">ClusPropertyValue</a> 
      objects.</li>
<li>Is obtained from <a href="https://msdn.microsoft.com/53cff9ea-15e4-4408-8e25-23219b8cfe76">ClusProperty.Values</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

