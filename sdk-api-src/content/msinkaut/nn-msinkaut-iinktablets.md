---
UID: NN:msinkaut.IInkTablets
title: IInkTablets (msinkaut.h)
description: .
helpviewer_keywords: ["IInkTablets","IInkTablets interface [Tablet PC]","IInkTablets interface [Tablet PC]","described","msinkaut/IInkTablets","tablet.iinktablets"]
old-location: tablet\iinktablets.htm
tech.root: tablet
ms.assetid: 98052ECB-9385-45C9-A03C-3F312ADD9872
ms.date: 12/05/2018
ms.keywords: IInkTablets, IInkTablets interface [Tablet PC], IInkTablets interface [Tablet PC],described, msinkaut/IInkTablets, tablet.iinktablets
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkTablets
 - msinkaut/IInkTablets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkTablets
---

# IInkTablets interface


## -description

Represents the object used to capture ink from available tablet devices.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablets</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkTablets</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkTablets</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-ispacketpropertysupported">IsPacketPropertySupported</a>
</td>
<td align="left" width="63%">
Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. For example, use this method to determine if all of the tablets in a collection support tangential pressure from a pen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object at the specified index within the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablets</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of objects or collections contained in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-get_defaulttablet">DefaultTablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the default tablet within the set of available tablets.

</td>
</tr>
</table>

## -remarks

Creating the InkCollector control behind a transparent control (such as a GroupBox with the WS_EX_TRANSPARENT property set) will prevent InkCollector from collecting ink.

## -see-also

[InkCollector class](/windows/win32/tablet/inkcollector-class)

