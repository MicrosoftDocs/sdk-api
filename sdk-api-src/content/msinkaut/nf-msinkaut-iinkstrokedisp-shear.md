---
UID: NF:msinkaut.IInkStrokeDisp.Shear
title: IInkStrokeDisp::Shear method
author: windows-driver-content
description: Shears the ink in the stroke or strokes by the specified horizontal and vertical factors.
old-location: tablet\iinkstrokedisp_shear.htm
old-project: tablet
ms.assetid: 887dd883-1a24-4a78-8f08-f4cd45bf4840
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 887dd883-1a24-4a78-8f08-f4cd45bf4840, IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], Shear method, IInkStrokeDisp::Shear, Shear method [Tablet PC], Shear method [Tablet PC], IInkStrokeDisp interface, Shear,IInkStrokeDisp.Shear, msinkaut/IInkStrokeDisp::Shear, tablet.iinkstrokedisp_shear
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.Shear
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkStrokeDisp::Shear method


## -description



Shears the ink in the stroke or strokes by the specified horizontal and vertical factors.




## -parameters




### -param HorizontalMultiplier [in]

The horizontal factor of the shear.


### -param VerticalMultiplier [in]

The vertical factor of the shear.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



The transformation applied in this method is a pure shear only if one of the parameters is 0. Applied to a rectangle at the origin, when the <i>shearY</i> factor is 0, the transformation moves the bottom edge horizontally by <i>shearX</i> times the height of the rectangle. When the <i>shearX</i> factor is 0, it moves the right edge vertically by <i>shearY</i> times the width of the rectangle.

<div class="alert"><b>Note</b>  When both parameters are nonzero, the results may not be intuitive.</div>
<div> </div>
This method throws an exception if the shear is non-invertible. The shear is non-invertible if the product of the <i>shearX</i> and <i>shearY</i> parameters equals 1.




## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

