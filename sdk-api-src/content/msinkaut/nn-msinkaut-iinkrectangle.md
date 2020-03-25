---
UID: NN:msinkaut.IInkRectangle
title: IInkRectangle (msinkaut.h)
description: .
old-location: tablet\iinkrectangle.htm
tech.root: tablet
ms.assetid: 9E438012-0991-46AA-8D0F-2C561F523EC2
ms.date: 12/05/2018
ms.keywords: IInkRectangle, IInkRectangle interface [Tablet PC], IInkRectangle interface [Tablet PC],described, msinkaut/IInkRectangle, tablet.iinkrectangle
f1_keywords:
- msinkaut/IInkRectangle
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msinkaut.h
api_name:
- IInkRectangle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRectangle interface


## -description

Represents an ink rectangle.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRectangle</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRectangle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkRectangle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle">GetRectangle</a>
</td>
<td align="left" width="63%">
Gets the elements of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object in a single call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle">SetRectangle</a>
</td>
<td align="left" width="63%">
Sets the elements of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object in a single call.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRectangle</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the bottom position of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data">Data</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets access to the rectangle structure (C++ only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the left position of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right">Right</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the right position of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top">Top</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the top position of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.

</td>
</tr>
</table> 

## -see-also

[InkRectangle class](https://docs.microsoft.com/windows/win32/tablet/inkrectangle-class)