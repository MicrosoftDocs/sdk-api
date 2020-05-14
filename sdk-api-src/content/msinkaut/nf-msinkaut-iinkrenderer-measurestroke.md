---
UID: NF:msinkaut.IInkRenderer.MeasureStroke
title: IInkRenderer::MeasureStroke (msinkaut.h)
description: Calculates the rectangle on the device context that would contain a stroke if it were drawn with the InkRenderer object using the DrawStroke method.helpviewer_keywords: ["IInkRenderer interface [Tablet PC]","MeasureStroke method","IInkRenderer.MeasureStroke","IInkRenderer::MeasureStroke","MeasureStroke","MeasureStroke method [Tablet PC]","MeasureStroke method [Tablet PC]","IInkRenderer interface","bdaee1c8-ff03-470f-b508-3db5391b3cf7","msinkaut/IInkRenderer::MeasureStroke","tablet.inkrenderer_measurestroke"]
old-location: tablet\inkrenderer_measurestroke.htm
tech.root: tablet
ms.assetid: bdaee1c8-ff03-470f-b508-3db5391b3cf7
ms.date: 12/05/2018
ms.keywords: IInkRenderer interface [Tablet PC],MeasureStroke method, IInkRenderer.MeasureStroke, IInkRenderer::MeasureStroke, MeasureStroke, MeasureStroke method [Tablet PC], MeasureStroke method [Tablet PC],IInkRenderer interface, bdaee1c8-ff03-470f-b508-3db5391b3cf7, msinkaut/IInkRenderer::MeasureStroke, tablet.inkrenderer_measurestroke
f1_keywords:
- msinkaut/IInkRenderer.MeasureStroke
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkRenderer.MeasureStroke
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRenderer::MeasureStroke


## -description



Calculates the rectangle on the device context that would contain a stroke if it were drawn with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object using the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a> method.




## -parameters




### -param Stroke [in]

The stroke to measure.


### -param DrawingAttributes [in, optional]

Optional. The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> to use when calculating the rectangle, which override the drawing attributes on the stroke. The default value is <b>NULL</b>, which means the stroke is measured by using its own drawing attributes.


### -param Rectangle [out, retval]

When this method returns, contains a pointer to the rectangle on the device context that would contain the stroke if the stroke were drawn with the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a> method of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object. The stroke must contain x- and y-coordinates to calculate the rectangle. Otherwise, the method returns an empty rectangle.


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
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object is not registered on the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> does not point to a compatible <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, or <i>drawingAttributes</i> is an invalid input parameter.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>
 




## -remarks



This is accurate only if you pass the same arguments to both <b>MeasureStroke</b> and <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a>.

Since the bounding box is affected by the pen width, this width is scaled appropriately for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a>'s view transform. To do this, the pen width is multiplied by the square root of the determinant of the view transform. The height and width of the bounding box are expanded by half this amount in each direction, and the right and bottom sides are incremented by one.

For example, consider that the pen width is originally 53, the square root of the determinant of the view transform is 50, and the bounding box is (0, 0, 1000, 1000). The pen width adjustment to the bounding box in each direction is calculated as (53 * 50) / 2, and the right and bottom sides are incremented by one. This results in a rendered bounding box of (-1325, -1325, 2326, 2326).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw">Draw Method [InkRenderer Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846805(v=VS.85).aspx">IInkRenderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure">Measure Method</a>
 

 

