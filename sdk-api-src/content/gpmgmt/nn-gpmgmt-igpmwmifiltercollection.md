---
UID: NN:gpmgmt.IGPMWMIFilterCollection
title: IGPMWMIFilterCollection (gpmgmt.h)
description: The IGPMWMIFilterCollection interface contains methods that enable applications to access a collection of WMI filters when using the Group Policy Management Console (GPMC) interfaces.helpviewer_keywords: ["GPMWMIFilterCollection","IGPMWMIFilterCollection","IGPMWMIFilterCollection interface [GPMC]","IGPMWMIFilterCollection interface [GPMC]","described","_win32_igpmwmifiltercollection","gpmc.igpmwmifiltercollection","gpmgmt/IGPMWMIFilterCollection"]
old-location: gpmc\igpmwmifiltercollection.htm
tech.root: gpmc
ms.assetid: 8f65e6f6-fca3-46b7-aa0d-804470feb5bb
ms.date: 12/05/2018
ms.keywords: GPMWMIFilterCollection, IGPMWMIFilterCollection, IGPMWMIFilterCollection interface [GPMC], IGPMWMIFilterCollection interface [GPMC],described, _win32_igpmwmifiltercollection, gpmc.igpmwmifiltercollection, gpmgmt/IGPMWMIFilterCollection
f1_keywords:
- gpmgmt/IGPMWMIFilterCollection
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMWMIFilterCollection interface


## -description


The 
<b>IGPMWMIFilterCollection</b>  interface contains methods that enable applications to access a collection of WMI filters when using the Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMWMIFilterCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMWMIFilterCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmwmifiltercollection-get__newenum">get__NewEnum</a>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
 

 

