---
UID: NF:msinkaut.IInkStrokes.ScaleToRectangle
title: IInkStrokes::ScaleToRectangle (msinkaut.h)
description: Scales the IInkStrokeDisp object or InkStrokes collection to fit in the specified InkRectangle object. (IInkStrokes.ScaleToRectangle)
helpviewer_keywords: ["8bc22004-3781-4018-9a92-88958039248c","IInkStrokes interface [Tablet PC]","ScaleToRectangle method","IInkStrokes.ScaleToRectangle","IInkStrokes::ScaleToRectangle","ScaleToRectangle","ScaleToRectangle method [Tablet PC]","ScaleToRectangle method [Tablet PC]","IInkStrokes interface","msinkaut/IInkStrokes::ScaleToRectangle","tablet.inkstrokes_scaletorectangle"]
old-location: tablet\inkstrokes_scaletorectangle.htm
tech.root: tablet
ms.assetid: 592b28e7-2bde-497d-8a15-2a1b4cc509b1
ms.date: 12/05/2018
ms.keywords: 8bc22004-3781-4018-9a92-88958039248c, IInkStrokes interface [Tablet PC],ScaleToRectangle method, IInkStrokes.ScaleToRectangle, IInkStrokes::ScaleToRectangle, ScaleToRectangle, ScaleToRectangle method [Tablet PC], ScaleToRectangle method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::ScaleToRectangle, tablet.inkstrokes_scaletorectangle
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
 - IInkStrokes::ScaleToRectangle
 - msinkaut/IInkStrokes::ScaleToRectangle
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
 - IInkStrokes.ScaleToRectangle
---

# IInkStrokes::ScaleToRectangle


## -description

Scales the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to fit in the specified <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.

## -parameters

### -param Rectangle [in]

The <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> in ink space to which the stroke or collection of strokes is scaled. The strokes are scaled and translated to match the strokes' bounding box to the rectangle.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
