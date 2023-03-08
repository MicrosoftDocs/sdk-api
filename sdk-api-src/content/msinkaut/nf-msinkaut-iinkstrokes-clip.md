---
UID: NF:msinkaut.IInkStrokes.Clip
title: IInkStrokes::Clip (msinkaut.h)
description: Removes portions of an IInkStrokeDisp object or InkStrokes collection that are outside a rectangle. (IInkStrokes.Clip)
helpviewer_keywords: ["Clip","Clip method [Tablet PC]","Clip method [Tablet PC]","IInkStrokes interface","IInkStrokes interface [Tablet PC]","Clip method","IInkStrokes.Clip","IInkStrokes::Clip","d3733613-fc8e-41f2-9172-07b61fc133dd","msinkaut/IInkStrokes::Clip","tablet.inkstrokes_clip"]
old-location: tablet\inkstrokes_clip.htm
tech.root: tablet
ms.assetid: ef434bcc-610c-449d-90d4-b3f897408f34
ms.date: 12/05/2018
ms.keywords: Clip, Clip method [Tablet PC], Clip method [Tablet PC],IInkStrokes interface, IInkStrokes interface [Tablet PC],Clip method, IInkStrokes.Clip, IInkStrokes::Clip, d3733613-fc8e-41f2-9172-07b61fc133dd, msinkaut/IInkStrokes::Clip, tablet.inkstrokes_clip
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokes::Clip
 - msinkaut/IInkStrokes::Clip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokes.Clip
---

# IInkStrokes::Clip


## -description

Removes portions of an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that are outside a rectangle.

## -parameters

### -param Rectangle [in]

Specifies the rectangle outside of which the stroke or strokes are clipped. The rectangle is specified in ink space coordinates.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid clip rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

For an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, all strokes intersected by the rectangle are split at the intersection points. All portions of strokes outside the rectangle are removed from the <b>InkDisp</b> object. The method may add new points to a stroke at the point where the stroke intersects the rectangle. After you call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip">Clip</a> method on an <b>InkDisp</b> object, the IDs of the strokes in the <b>InkDisp</b> object's strokes collection are guaranteed to be unique, but not guaranteed to preserve other information.

This method does not take the pen width into account when clipping. It clips only the actual ink or stroke data.

For an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection, the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip">Clip</a> method updates the parent <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. Whenever ink is removed from an <b>InkDisp</b> object, any <b>IInkStrokeDisp</b> objects or InkStrokes collections defined for that <b>InkDisp</b> object may be invalidated.

For more information on ink data, see <a href="/windows/desktop/tablet/ink-data">Ink Data</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle">HitTest(Rectangle, Single) Method</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
