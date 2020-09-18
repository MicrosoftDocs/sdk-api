---
UID: NF:ocidl.IViewObjectEx.QueryHitRect
title: IViewObjectEx::QueryHitRect (ocidl.h)
description: Indicates whether any point in a rectangle is within a given drawing aspect of an object.
helpviewer_keywords: ["IViewObjectEx interface [COM]","QueryHitRect method","IViewObjectEx.QueryHitRect","IViewObjectEx::QueryHitRect","QueryHitRect","QueryHitRect method [COM]","QueryHitRect method [COM]","IViewObjectEx interface","_ole_iviewobjectex_queryhitrect","com.iviewobjectex_queryhitrect","ocidl/IViewObjectEx::QueryHitRect"]
old-location: com\iviewobjectex_queryhitrect.htm
tech.root: com
ms.assetid: eb155424-e74c-497f-a9c0-33ed3b2b5513
ms.date: 12/05/2018
ms.keywords: IViewObjectEx interface [COM],QueryHitRect method, IViewObjectEx.QueryHitRect, IViewObjectEx::QueryHitRect, QueryHitRect, QueryHitRect method [COM], QueryHitRect method [COM],IViewObjectEx interface, _ole_iviewobjectex_queryhitrect, com.iviewobjectex_queryhitrect, ocidl/IViewObjectEx::QueryHitRect
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
 - IViewObjectEx::QueryHitRect
 - ocidl/IViewObjectEx::QueryHitRect
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
 - IViewObjectEx.QueryHitRect
---

# IViewObjectEx::QueryHitRect


## -description

Indicates whether any point in a rectangle is within a given drawing aspect of an object.

## -parameters

### -param dwAspect [in]

The requested drawing aspect.

### -param pRectBounds [in]

An object bounding rectangle in client coordinates of the containing window. This rectangle is computed and passed by the container so that the object can meaningfully interpret the hit location.

### -param pRectLoc [in]

The hit test rectangle, specified in <b>HIMETRIC</b> units, relative to the top-left corner of the object.

### -param lCloseHint [in]

The suggested distance, in <b>HIMETRIC</b> units, that the container considers close. This value is a hint, and objects can interpret it in their own way. Objects can also use this hint to roughly infer output resolution to choose expansiveness of hit test implementation.

### -param pHitResult [out]

A pointer to returned information about the hit expressed as the <a href="/windows/desktop/api/ocidl/ne-ocidl-hitresult">HITRESULT</a> enumeration values.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented for the requested aspect. Use DVASPECT_CONTENT instead.

</td>
</tr>
</table>

## -remarks

Containers may need to test whether an object overlaps a given drawing aspect of another object. They can determine whether the objects overlap by requesting a region or at least a bounding rectangle of the aspect in question. However, a quicker way to do this is to call <b>IViewObjectEx::QueryHitRect</b> to ask the object whether a given rectangle intersects one of its drawing aspects.

<div class="alert"><b>Note</b>  Unlike <a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-queryhitpoint">IViewObjectEx::QueryHitPoint</a>, this method does not return HITRESULT_TRANSPARENT or HITRESULT_CLOSE. It is strictly hit or miss, returning HITRESULT_OUTSIDE if no point in the rectangle is hit and HITRESULT_HIT if at least one point in the rectangle is a hit.</div>
<div> </div>
<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object supporting <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> is required to implement this method at least for the DVASPECT_CONTENT aspect. The object should not take any other action in response to this method other than to return the information; there should be no side-effects. If there is any ambiguity about whether a point is a hit, for instance due to coordinates not converting exactly, the object should return HITRESULT_HIT whenever any point in the rectangle might be a hit on the object. That is, it is permissible to claim a hit for a point that is not actually rendered, but never correct to claim a miss for any point that is in the rendered image of the object.

## -see-also

<a href="/windows/desktop/api/ocidl/ne-ocidl-hitresult">HITRESULT</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a>