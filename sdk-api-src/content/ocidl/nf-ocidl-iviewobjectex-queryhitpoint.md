---
UID: NF:ocidl.IViewObjectEx.QueryHitPoint
title: IViewObjectEx::QueryHitPoint (ocidl.h)
description: Indicates whether a point is within a given aspect of an object.
helpviewer_keywords: ["IViewObjectEx interface [COM]","QueryHitPoint method","IViewObjectEx.QueryHitPoint","IViewObjectEx::QueryHitPoint","QueryHitPoint","QueryHitPoint method [COM]","QueryHitPoint method [COM]","IViewObjectEx interface","_ole_iviewobjectex_queryhitpoint","com.iviewobjectex_queryhitpoint","ocidl/IViewObjectEx::QueryHitPoint"]
old-location: com\iviewobjectex_queryhitpoint.htm
tech.root: com
ms.assetid: a9ee26c4-cf5f-4ca9-b40a-0522097a2f07
ms.date: 12/05/2018
ms.keywords: IViewObjectEx interface [COM],QueryHitPoint method, IViewObjectEx.QueryHitPoint, IViewObjectEx::QueryHitPoint, QueryHitPoint, QueryHitPoint method [COM], QueryHitPoint method [COM],IViewObjectEx interface, _ole_iviewobjectex_queryhitpoint, com.iviewobjectex_queryhitpoint, ocidl/IViewObjectEx::QueryHitPoint
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
 - IViewObjectEx::QueryHitPoint
 - ocidl/IViewObjectEx::QueryHitPoint
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
 - IViewObjectEx.QueryHitPoint
---

# IViewObjectEx::QueryHitPoint


## -description

Indicates whether a point is within a given aspect of an object.

## -parameters

### -param dwAspect [in]

The requested drawing aspect.

### -param pRectBounds [in]

An object bounding rectangle in client coordinates of the containing window. This rectangle is computed and 
       passed by the container so that the object can meaningfully interpret the hit location.

### -param ptlLoc [in]

The hit location in client coordinates of the containing window.

### -param lCloseHint [in]

Suggested distance in <b>HIMETRIC</b> units that the container considers close. This 
       value is a hint, and objects can interpret it in their own way. Objects can also use this hint to roughly infer 
       output resolution to choose expansiveness of hit test implementation.

### -param pHitResult [out]

A pointer to returned information about the hit expressed as the 
       <a href="/windows/desktop/api/ocidl/ne-ocidl-hitresult">HITRESULT</a> enumeration values.

## -returns

This method returns <b>S_OK</b> on success. Other possible return values include the 
       following.

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
This method is not implemented for the requested aspect. Use 
         <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT_CONTENT</a> instead.

</td>
</tr>
</table>

## -remarks

To support hit detection on non-rectangular objects, the container needs a reliable way to ask an object 
     whether a given location is inside one of its drawing aspects. This function is provided by 
     <b>IViewObjectEx::QueryHitPoint</b>.

<div class="alert"><b>Note</b>  Because this method is part of the <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> 
     interface, the container can figure whether a mouse hit is over an object without having to necessarily launch 
     the server. If the hit happens to be inside the object, then it is likely that the object will be in-place 
     activated and the server started.</div>
<div> </div>
Typically, the container first quickly determines whether a given location is within the rectangular extent of 
     an object. If the location is within the rectangular extent of an object, the container calls 
     <b>IViewObjectEx::QueryHitPoint</b> to get 
     confirmation that the location is actually inside the object. The hit location is passed in client coordinates of 
     the container window. Since the object may be inactive when this method is called, the bounding rectangle of the 
     object in the same coordinate system is also passed to this method, similarly to what happens in 
     <a href="/windows/desktop/api/ocidl/nf-ocidl-ipointerinactive-oninactivesetcursor">IPointerInactive::OnInactiveSetCursor</a>.

Possible returned values include:

<ul>
<li>Outside, on a transparent region</li>
<li>Close enough to be considered a hit (may be used by small or thin objects)</li>
<li>Hit</li>
</ul>
<b>IViewObjectEx::QueryHitPoint</b> is not 
     concerned by the sub-objects of the object it is called for. It merely indicates whether the mouse hit was within 
     the object or not.

<b>IViewObjectEx::QueryHitPoint</b> can be called 
     for any of the drawing aspects an object supports. It should fail if the it is not supported for the requested 
     drawing aspect.

Transparent objects may wish to implement a complex hit-detection mechanism where the user can select either 
     the transparent object or an object behind it, depending on where exactly the click happens inside the object. 
     For example, a transparent text box showing big enough text may let the user select the object behind, for 
     example, a bitmap, when the user clicks between the characters. For this reason, the information returned by 
     <b>IViewObjectEx::QueryHitPoint</b> includes 
     indication about whether the hit happens on an opaque or transparent region.

An example of non-rectangular and transparent hit detection is a transparent circle control with an object 
     behind it (a line in the example below):

:::image type="content" source="./images/a7c7fe0d-f171-4823-ba4c-b51cb90d8733.png" border="false" alt-text="Diagram of a circle with a diagonal line through it, showing the hit detection values for the areas inside and outside the circle and near the line.":::

The values shown are for hit tests against the circle; gray regions are not part of the control, but are shown 
     here to indicate an area around the image considered close. Each object implements its own definition of close 
     but is assisted by a hint provided by the container so that closeness can be adjusted as images zoom larger or 
     smaller.

In the picture above, the points marked Hit, Close, and Transparent would all be hits of varying strength on 
     the circle, with the exception of the one marked Transparent, (but for the line, close). This illustrates the 
     effect of the different strength of hits. Because the circle responds transparent while the line claims close, 
     and transparent is weaker than close, the line takes the hit.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object supporting <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> is required to 
      implement this method at least for the <b>DVASPECT_CONTENT</b> aspect. The object should 
      not take any other action in response to this method other than to return the information; there should be no 
      side-effects.

## -see-also

<a href="/windows/desktop/api/ocidl/ne-ocidl-hitresult">HITRESULT</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipointerinactive-oninactivesetcursor">IPointerInactive::OnInactiveSetCursor</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a>