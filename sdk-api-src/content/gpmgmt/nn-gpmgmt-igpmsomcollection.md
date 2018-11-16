---
UID: NN:gpmgmt.IGPMSOMCollection
title: IGPMSOMCollection
author: windows-sdk-content
description: The IGPMSOMCollection interface represents a collection of GPMSOM objects.
old-location: gpmc\igpmsomcollection.htm
tech.root: GPMC
ms.assetid: 079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GPMSOMCollection, IGPMSOMCollection, IGPMSOMCollection interface [GPMC], IGPMSOMCollection interface [GPMC],described, _win32_igpmsomcollection, gpmc.igpmsomcollection, gpmgmt/IGPMSOMCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGPMSOMCollection
 - IGPMSOMCollection.Count
 - IGPMSOMCollection.get_Count
 - IGPMSOMCollection.Item
 - IGPMSOMCollection.get_Item
 - GPMSOMCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMSOMCollection interface


## -description


The 
<b>IGPMSOMCollection</b> interface represents a collection of 
<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">GPMSOM</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOMCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMSOMCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMSOMCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e6a33d8-5435-4ae9-93e7-439441d0f098">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOMCollection</b> interface has these properties.
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
Number of SOM entries in this collection.

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



<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>
 

 

