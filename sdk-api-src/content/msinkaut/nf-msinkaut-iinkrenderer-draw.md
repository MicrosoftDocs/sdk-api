---
UID: NF:msinkaut.IInkRenderer.Draw
title: IInkRenderer::Draw (msinkaut.h)
description: Draws ink strokes using the known device context.
helpviewer_keywords: ["18f67080-ed56-43af-b0d6-8af35c2e871b","Draw","Draw method [Tablet PC]","Draw method [Tablet PC]","IInkRenderer interface","IInkRenderer","IInkRenderer interface [Tablet PC]","Draw method","IInkRenderer.Draw","IInkRenderer::Draw","msinkaut/IInkRenderer::Draw","tablet.inkrenderer_draw"]
old-location: tablet\inkrenderer_draw.htm
tech.root: tablet
ms.assetid: 18f67080-ed56-43af-b0d6-8af35c2e871b
ms.date: 12/05/2018
ms.keywords: 18f67080-ed56-43af-b0d6-8af35c2e871b, Draw, Draw method [Tablet PC], Draw method [Tablet PC],IInkRenderer interface, IInkRenderer, IInkRenderer interface [Tablet PC],Draw method, IInkRenderer.Draw, IInkRenderer::Draw, msinkaut/IInkRenderer::Draw, tablet.inkrenderer_draw
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
 - IInkRenderer::Draw
 - msinkaut/IInkRenderer::Draw
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
 - IInkRenderer.Draw
---

# IInkRenderer::Draw


## -description

Draws ink strokes using the known device context.

## -parameters

### -param hDC [in]

Specifies the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a> of the device context on which to draw.

### -param Strokes [in]

Specifies the strokes to draw.

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
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The strokes parameter is associated with a different <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <i>hdc</i> or the <i>strokes</i> parameter does not point to a valid object.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>

## -remarks

The pen width is multiplied (or scaled) by the square root of the determinant of the view transform.

<div class="alert"><b>Note</b>  If you have not set the pen width explicitly, it is 53 by default. You must multiply the pen width by the square root of the determinant to yield the correct bounding box. The height and width of the bounding box are expanded by half this amount in each direction.</div>
<div> </div>
For example, consider that the pen width is 53, the square root of the determinant is 50, and the bounding box is (0,0,1000,1000). The pen width adjustment to the bounding box in each direction is calculated as (53*50)/2, and the right and bottom sides are incremented by one. This results in a rendered bounding box of (-1325,-1325,2326,2326).

<div class="alert"><b>Note</b>  Use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a> method to draw a single stroke.</div>
<div> </div>
The <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> forces the viewport and window origins to 0, 0. Any existing settings are saved and restored, but is not used by the <b>InkRenderer</b>. To perform scrolling, use the <b>InkRenderer</b> object's view and object transform methods.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke Method</a>



<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
