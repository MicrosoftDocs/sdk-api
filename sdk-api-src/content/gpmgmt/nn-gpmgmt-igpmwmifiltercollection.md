---
UID: NN:gpmgmt.IGPMWMIFilterCollection
title: IGPMWMIFilterCollection
author: windows-sdk-content
description: The IGPMWMIFilterCollection interface contains methods that enable applications to access a collection of WMI filters when using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmwmifiltercollection.htm
tech.root: gpmc
ms.assetid: 8f65e6f6-fca3-46b7-aa0d-804470feb5bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GPMWMIFilterCollection, IGPMWMIFilterCollection, IGPMWMIFilterCollection interface [GPMC], IGPMWMIFilterCollection interface [GPMC],described, _win32_igpmwmifiltercollection, gpmc.igpmwmifiltercollection, gpmgmt/IGPMWMIFilterCollection
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
 - IGPMWMIFilterCollection
 - IGPMWMIFilterCollection.Count
 - IGPMWMIFilterCollection.get_Count
 - IGPMWMIFilterCollection.Item
 - IGPMWMIFilterCollection.get_Item
 - GPMWMIFilterCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMWMIFilterCollection interface


## -description


The 
<b>IGPMWMIFilterCollection</b>  interface contains methods that enable applications to access a collection of WMI filters when using the Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMWMIFilterCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMWMIFilterCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMWMIFilterCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acba6a75-9338-49b8-b04b-829f527d92ce">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMWMIFilterCollection</b> interface has these properties.
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
Number of WMI filters in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific WMI filter from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>
 

 

