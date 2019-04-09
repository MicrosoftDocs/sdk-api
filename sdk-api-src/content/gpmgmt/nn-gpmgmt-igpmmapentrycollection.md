---
UID: NN:gpmgmt.IGPMMapEntryCollection
title: IGPMMapEntryCollection (gpmgmt.h)
author: windows-sdk-content
description: The IGPMMapEntryCollection interface enables applications to access map entry objects.
old-location: gpmc\igpmmapentrycollection.htm
tech.root: gpmc
ms.assetid: a017ff4b-ab3c-4da9-b6c9-b4ccd24230eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMMapEntryCollection, IGPMMapEntryCollection, IGPMMapEntryCollection interface [GPMC], IGPMMapEntryCollection interface [GPMC],described, gpmc.igpmmapentrycollection, gpmgmt/IGPMMapEntryCollection
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMapEntryCollection
 - IGPMMapEntryCollection.Count
 - IGPMMapEntryCollection.get_Count
 - IGPMMapEntryCollection.Item
 - IGPMMapEntryCollection.get_Item
 - GPMMapEntryCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMMapEntryCollection interface


## -description


The <b>IGPMMapEntryCollection</b> interface enables applications to access map entry objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMMapEntryCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMMapEntryCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMMapEntryCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c169028-e87f-45d2-aadd-c403699cfd73">get__NewEnum</a>
</td>
<td align="left" width="63%">
Returns an enumerator over the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMMapEntryCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Count</b>

</td>
<td align="left" width="63%">
Number of map entries in this collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific element from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>
 

 

