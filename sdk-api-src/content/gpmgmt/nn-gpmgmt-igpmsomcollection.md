---
UID: NN:gpmgmt.IGPMSOMCollection
title: IGPMSOMCollection (gpmgmt.h)
description: The IGPMSOMCollection interface represents a collection of GPMSOM objects.
helpviewer_keywords: ["GPMSOMCollection","IGPMSOMCollection","IGPMSOMCollection interface [GPMC]","IGPMSOMCollection interface [GPMC]","described","_win32_igpmsomcollection","gpmc.igpmsomcollection","gpmgmt/IGPMSOMCollection"]
old-location: gpmc\igpmsomcollection.htm
tech.root: gpmc
ms.assetid: 079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d
ms.date: 12/05/2018
ms.keywords: GPMSOMCollection, IGPMSOMCollection, IGPMSOMCollection interface [GPMC], IGPMSOMCollection interface [GPMC],described, _win32_igpmsomcollection, gpmc.igpmsomcollection, gpmgmt/IGPMSOMCollection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMSOMCollection
 - gpmgmt/IGPMSOMCollection
dev_langs:
 - c++
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
---

# IGPMSOMCollection interface


## -description

The 
<b>IGPMSOMCollection</b> interface represents a collection of 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">GPMSOM</a> objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOMCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMSOMCollection</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsomcollection-get__newenum">get__NewEnum</a>
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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>