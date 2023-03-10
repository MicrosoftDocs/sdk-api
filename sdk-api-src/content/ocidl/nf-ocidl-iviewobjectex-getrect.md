---
UID: NF:ocidl.IViewObjectEx.GetRect
title: IViewObjectEx::GetRect (ocidl.h)
description: Retrieves a rectangle describing a requested drawing aspect.
helpviewer_keywords: ["GetRect","GetRect method [COM]","GetRect method [COM]","IViewObjectEx interface","IViewObjectEx interface [COM]","GetRect method","IViewObjectEx.GetRect","IViewObjectEx::GetRect","_ole_iviewobjectex_getrect","com.iviewobjectex_getrect","ocidl/IViewObjectEx::GetRect"]
old-location: com\iviewobjectex_getrect.htm
tech.root: com
ms.assetid: ff060cd2-c7e4-4c12-842a-663415b80c17
ms.date: 12/05/2018
ms.keywords: GetRect, GetRect method [COM], GetRect method [COM],IViewObjectEx interface, IViewObjectEx interface [COM],GetRect method, IViewObjectEx.GetRect, IViewObjectEx::GetRect, _ole_iviewobjectex_getrect, com.iviewobjectex_getrect, ocidl/IViewObjectEx::GetRect
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
 - IViewObjectEx::GetRect
 - ocidl/IViewObjectEx::GetRect
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
 - IViewObjectEx.GetRect
---

# IViewObjectEx::GetRect


## -description

Retrieves a rectangle describing a requested drawing aspect.

## -parameters

### -param dwAspect [in]

The drawing aspect requested.

### -param pRect [out]

A pointer to the rectangle describing the requested drawing aspect.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
The method does not support the specified aspect. Either the object does not support the aspect requested or the aspect is not rectangular.

</td>
</tr>
</table>

## -remarks

This method returns a rectangle describing the specified drawing aspect. The returned rectangle is in <b>HIMETRIC</b> units, relative to the object's origin. The rectangle returned depends on the drawing aspect as follows.

<table>
<tr>
<th>Drawing Aspect</th>
<th>Description</th>
</tr>
<tr>
<td>
DVASPECT_CONTENT

</td>
<td>
Objects should return the bounding rectangle of the whole object. The top-left corner is at the object's origin and the size is equal to the extent returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject2-getextent">IViewObject2::GetExtent</a>.

</td>
</tr>
<tr>
<td>
DVASPECT_OPAQUE

</td>
<td>
Objects with a rectangular opaque region should return that rectangle. Others should fail and return error code DV_E_DVASPECT.

If a rectangle is returned, it is guaranteed to be completely obscured by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> for that aspect. The container should use that rectangle to clip out the object's opaque parts before drawing any object behind it during the back to front pass. If this method fails on an object with a non-rectangular opaque region, the container should draw the entire object in the back to front part using the DVASPECT_CONTENT aspect.

</td>
</tr>
<tr>
<td>
DVASPECT_TRANSPARENT

</td>
<td>
Objects should return the rectangle covering all transparent or irregular parts. If the object does not have any transparent or irregular parts, it may return DV_E_ASPECT. A container may use this rectangle to determine whether there are other objects overlapping the transparent parts of a given object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a>