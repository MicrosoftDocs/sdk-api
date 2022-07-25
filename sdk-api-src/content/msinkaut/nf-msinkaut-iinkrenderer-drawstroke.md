---
UID: NF:msinkaut.IInkRenderer.DrawStroke
title: IInkRenderer::DrawStroke (msinkaut.h)
description: Draws the IInkStrokeDisp object using the known device context, and optionally draws the IInkStrokeDisp object with the known InkDrawingAttributes object.
helpviewer_keywords: ["3d8b7892-a120-452a-b83c-474df9be5f52","DrawStroke","DrawStroke method [Tablet PC]","DrawStroke method [Tablet PC]","IInkRenderer interface","IInkRenderer interface [Tablet PC]","DrawStroke method","IInkRenderer.DrawStroke","IInkRenderer::DrawStroke","msinkaut/IInkRenderer::DrawStroke","tablet.inkrenderer_drawstroke"]
old-location: tablet\inkrenderer_drawstroke.htm
tech.root: tablet
ms.assetid: 3d8b7892-a120-452a-b83c-474df9be5f52
ms.date: 12/05/2018
ms.keywords: 3d8b7892-a120-452a-b83c-474df9be5f52, DrawStroke, DrawStroke method [Tablet PC], DrawStroke method [Tablet PC],IInkRenderer interface, IInkRenderer interface [Tablet PC],DrawStroke method, IInkRenderer.DrawStroke, IInkRenderer::DrawStroke, msinkaut/IInkRenderer::DrawStroke, tablet.inkrenderer_drawstroke
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
 - IInkRenderer::DrawStroke
 - msinkaut/IInkRenderer::DrawStroke
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
 - IInkRenderer.DrawStroke
---

# IInkRenderer::DrawStroke


## -description

Draws the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object using the known device context, and optionally draws the <b>IInkStrokeDisp</b> object with the known <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

## -parameters

### -param hDC [in]

 The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a> of the device context on which to draw.

### -param Stroke [in]

 The stroke to draw.

### -param DrawingAttributes [in, optional]

Optional. Specifies the <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> to use on the drawing. The default value is <b>NULL</b>. If <b>InkDrawingAttributes</b> is specified, they override the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> on the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a>.

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
Invalid display handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <i>stroke</i> or the <i>drawingAttributes</i> parameter does not point to a valid object.

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

The <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> forces the viewport and window origins to 0, 0. Any existing settings are saved and restored, but are not used by the <b>InkRenderer</b>. To perform scrolling, use the <b>InkRenderer</b> object's view and object transform methods.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw">Draw Method [InkRenderer Class]</a>



<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>
