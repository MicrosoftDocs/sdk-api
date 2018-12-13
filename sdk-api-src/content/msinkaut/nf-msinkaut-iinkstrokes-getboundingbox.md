---
UID: NF:msinkaut.IInkStrokes.GetBoundingBox
title: IInkStrokes::GetBoundingBox
author: windows-sdk-content
description: Gets the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or an InkStrokes collection.
old-location: tablet\inkstrokes_getboundingbox.htm
tech.root: tablet
ms.assetid: 33641615-c2dc-43ee-b7be-8f24c38bac6b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 3b2c8cfc-05e6-4b53-b709-72291ee78471, GetBoundingBox, GetBoundingBox method [Tablet PC], GetBoundingBox method [Tablet PC],IInkStrokes interface, IInkStrokes interface [Tablet PC],GetBoundingBox method, IInkStrokes.GetBoundingBox, IInkStrokes::GetBoundingBox, msinkaut/IInkStrokes::GetBoundingBox, tablet.inkstrokes_getboundingbox
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
 - IInkStrokes.GetBoundingBox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokes::GetBoundingBox


## -description



Gets the bounding box in ink space coordinates for either all of the strokes in an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, an individual stroke, or an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.




## -parameters




### -param BoundingBoxMode [in, optional]

Optional. Specifies the stroke characteristics to use to calculate the bounding box. For more details about the use of stroke characteristics to calculate a bounding box, see the <a href="https://msdn.microsoft.com/8c92fb43-1584-42fc-857e-aae5d5c222b4">BoundingBoxMode</a> enumeration type.

The <i>BoundingBoxMode</i> parameter of the <a href="https://msdn.microsoft.com/3b2c8cfc-05e6-4b53-b709-72291ee78471">GetBoundingBox</a> method has a default value of -1, which means that all characteristics of a stroke are used to specify the bounding box.


### -param BoundingBox [out, retval]

When this method returns, contains a pointer to the rectangle that defines the bounding box of an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object, or an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

<div class="alert"><b>Note</b>  For an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object, the returned bounding box is a copy of the strokes bounding box, so altering the returned bounding box does not affect the strokes location.</div>
<div> </div>

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
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a> object is not registered.

</td>
</tr>
</table>
 




## -remarks



When the bounding box is affected by the pen width, then this width is scaled appropriately for the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a>'s view transform. To do this, the pen width is multiplied by the square root of the determinant of the view transform.

<div class="alert"><b>Note</b>  In Windows Vista and later versions, <a href="https://msdn.microsoft.com/3b2c8cfc-05e6-4b53-b709-72291ee78471">GetBoundingBox Method</a> does not take the width of the stroke into account.</div>
<div> </div>
<div class="alert"><b>Note</b>  If you have not set the pen width explicitly, it is 53 by default. You must multiply the pen width by the square root of the determinant to yield the correct bounding box. The height and width of the bounding box are expanded by half this amount in each direction. For example, consider that the pen width is 53, the square root of the determinant is 50, and the bounding box is (0, 0, 1000, 1000). The pen width adjustment to the bounding box in each direction is calculated as (53 * 50) / 2, and the right and bottom sides are incremented by one. This results in a rendered bounding box of (-1325, -1325, 2326, 2326).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846806(v=VS.85).aspx">IInkStrokes</a>



<a href="https://msdn.microsoft.com/8c92fb43-1584-42fc-857e-aae5d5c222b4">InkBoundingBoxMode Enumeration</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

