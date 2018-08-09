---
UID: NF:msinkaut.IInkRenderer.Draw
title: IInkRenderer::Draw
author: windows-sdk-content
description: Draws ink strokes using the known device context.
old-location: tablet\inkrenderer_draw.htm
old-project: tablet
ms.assetid: 18f67080-ed56-43af-b0d6-8af35c2e871b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 18f67080-ed56-43af-b0d6-8af35c2e871b, Draw, Draw method [Tablet PC], Draw method [Tablet PC],IInkRenderer interface, IInkRenderer, IInkRenderer interface [Tablet PC],Draw method, IInkRenderer.Draw, IInkRenderer::Draw, msinkaut/IInkRenderer::Draw, tablet.inkrenderer_draw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRenderer::Draw


## -description



Draws ink strokes using the known device context.




## -parameters




### -param hDC [in]

Specifies the <a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd</a> of the device context on which to draw.


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
The strokes parameter is associated with a different <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

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

<div class="alert"><b>Note</b>  Use the <a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a> method to draw a single stroke.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> forces the viewport and window origins to 0, 0. Any existing settings are saved and restored, but is not used by the <b>InkRenderer</b>. To perform scrolling, use the <b>InkRenderer</b> object's view and object transform methods.




## -see-also




<a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke Method</a>



<a href="tablet.iinkrenderer">IInkRenderer</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

