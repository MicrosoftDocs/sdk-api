---
UID: NF:msinkaut.IInkRenderer.Measure
title: IInkRenderer::Measure
author: windows-sdk-content
description: Calculates the rectangle on the device context that would contain a collection of strokes if the strokes were drawn with the InkRenderer object using the DrawStroke method.
old-location: tablet\inkrenderer_measure.htm
tech.root: tablet
ms.assetid: 1ef9ef91-ae96-454f-9ef8-570e64852395
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 1ef9ef91-ae96-454f-9ef8-570e64852395, IInkRenderer interface [Tablet PC],Measure method, IInkRenderer.Measure, IInkRenderer::Measure, Measure, Measure method [Tablet PC], Measure method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::Measure, tablet.inkrenderer_measure
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInkRenderer.Measure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRenderer::Measure


## -description



Calculates the rectangle on the device context that would contain a collection of strokes if the strokes were drawn with the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object using the <a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a> method.




## -parameters




### -param Strokes [in]

The collection of strokes to measure.


### -param Rectangle [out, retval]

When this method returns, contains a pointer to the rectangle on the device context that would contain the strokes if they were drawn with the <a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a> method of the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object. The strokes must contain x- and y-coordinates to calculate the rectangle. Otherwise, the method returns an empty rectangle.


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
The <i>strokes</i> parameter does not point to a valid object.

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



This is accurate only if you pass the same arguments to both <b>Measure</b> and <a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a>.

Since the bounding box is affected by the pen width, this width is scaled appropriately for the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a>'s view transform. To do this, the pen width is multiplied by the square root of the determinant of the view transform. The height and width of the bounding box are expanded by half this amount in each direction, and the right and bottom sides are incremented by one.

For example, consider that the pen width is originally 53, the square root of the determinant of the view transform is 50, and the bounding box is (0, 0, 1000, 1000). The pen width adjustment to the bounding box in each direction is calculated as (53 * 50) / 2, and the right and bottom sides are incremented by one. This results in a rendered bounding box of (-1325, -1325, 2326, 2326).




## -see-also




<a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw Method [InkRenderer Class]</a>



<a href="https://msdn.microsoft.com/2AB56616-3F67-4428-8A99-FCE733A5FDBF">IInkRenderer</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/bdaee1c8-ff03-470f-b508-3db5391b3cf7">MeasureStroke Method</a>
 

 

