---
UID: NF:ocidl.IOleInPlaceSiteWindowless.AdjustRect
title: IOleInPlaceSiteWindowless::AdjustRect (ocidl.h)
description: Adjusts a specified rectangle if it is entirely or partially covered by overlapping, opaque objects.
helpviewer_keywords: ["AdjustRect","AdjustRect method [COM]","AdjustRect method [COM]","IOleInPlaceSiteWindowless interface","IOleInPlaceSiteWindowless interface [COM]","AdjustRect method","IOleInPlaceSiteWindowless.AdjustRect","IOleInPlaceSiteWindowless::AdjustRect","_ole_ioleinplacesitewindowless_adjustrect","com.ioleinplacesitewindowless_adjustrect","ocidl/IOleInPlaceSiteWindowless::AdjustRect"]
old-location: com\ioleinplacesitewindowless_adjustrect.htm
tech.root: com
ms.assetid: 36fa395d-09b2-474d-85ae-5a22d25e88eb
ms.date: 12/05/2018
ms.keywords: AdjustRect, AdjustRect method [COM], AdjustRect method [COM],IOleInPlaceSiteWindowless interface, IOleInPlaceSiteWindowless interface [COM],AdjustRect method, IOleInPlaceSiteWindowless.AdjustRect, IOleInPlaceSiteWindowless::AdjustRect, _ole_ioleinplacesitewindowless_adjustrect, com.ioleinplacesitewindowless_adjustrect, ocidl/IOleInPlaceSiteWindowless::AdjustRect
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleInPlaceSiteWindowless::AdjustRect
 - ocidl/IOleInPlaceSiteWindowless::AdjustRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceSiteWindowless.AdjustRect
---

# IOleInPlaceSiteWindowless::AdjustRect


## -description

Adjusts a specified rectangle if it is entirely or partially covered by overlapping, opaque objects.

## -parameters

### -param prc [in, out]

The rectangle to be adjusted.

## -returns

This method returns S_OK if rectangle was adjusted successfully; meaning that the rectangle was not completely covered. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The rectangle was adjusted successfully. Note S_FALSE means that the rectangle was completely covered. Its width and height are now <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The main use of this method is to adjust the size of the caret. An object willing to create a caret should submit the caret rectangle to its site object by calling this method and using the adjusted rectangle returned from it for the caret. If the caret is entirely hidden, this method will return S_FALSE and the caret should not be shown at all in this case.

In a situation where objects are overlapping this method should return the largest rectangle that is fully visible.

This method can also be used to figure whether a point or a rectangular area is visible or hidden by overlapping objects.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>