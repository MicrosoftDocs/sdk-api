---
UID: NN:textstor.IAnchor
title: IAnchor (textstor.h)
description: The IAnchor interface is implemented by the TSF manager. Clients of Microsoft Active Accessibility use IAnchor anchor objects to delimit a range of text within a text stream.
helpviewer_keywords: ["IAnchor","IAnchor interface [Text Services Framework]","IAnchor interface [Text Services Framework]","described","textstor/IAnchor","tsf.ianchor"]
old-location: tsf\ianchor.htm
tech.root: TSF
ms.assetid: a7d52959-8386-464f-958d-c870f286b265
ms.date: 12/05/2018
ms.keywords: IAnchor, IAnchor interface [Text Services Framework], IAnchor interface [Text Services Framework],described, textstor/IAnchor, tsf.ianchor
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IAnchor
 - textstor/IAnchor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IAnchor
---

# IAnchor interface


## -description

The <b>IAnchor</b> interface is implemented by the TSF manager. Clients of <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a> use <b>IAnchor</b> anchor objects to delimit a range of text within a text stream.

The interface ID is IID_IAnchor.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnchor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAnchor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnchor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-clearchangehistory">ClearChangeHistory</a>
</td>
<td align="left" width="63%">
Clears the change history flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-clone">Clone</a>
</td>
<td align="left" width="63%">
Produces a new anchor object positioned at the same location, and with the same gravity, as the current anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-compare">Compare</a>
</td>
<td align="left" width="63%">
Compares the relative position of two anchors within a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-getchangehistory">GetChangeHistory</a>
</td>
<td align="left" width="63%">
Gets the change history of deletions that have occurred immediately preceding or following the anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-getgravity">GetGravity</a>
</td>
<td align="left" width="63%">
Retrieves the gravity of the anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Specifies the equality or inequality of the positions of two anchors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-setchangehistorymask">SetChangeHistoryMask</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-setgravity">SetGravity</a>
</td>
<td align="left" width="63%">
Sets the gravity of the anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-shift">Shift</a>
</td>
<td align="left" width="63%">
Shifts the anchor forward or backward.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-shiftregion">ShiftRegion</a>
</td>
<td align="left" width="63%">
Shifts the anchor into an adjacent region in the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-shiftto">ShiftTo</a>
</td>
<td align="left" width="63%">
Shifts the current anchor to the same position as another anchor.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>

