---
UID: NF:msinkaut.IInkTransform.Shear
title: IInkTransform::Shear
author: windows-sdk-content
description: Adjusts the shear of the InkTransform by the specified horizontal and vertical factors.
old-location: tablet\inktransform_shear.htm
old-project: tablet
ms.assetid: 4a3d828e-33cc-435f-9276-7c3304cca71d
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 4a3d828e-33cc-435f-9276-7c3304cca71d, IInkTransform interface [Tablet PC],Shear method, IInkTransform.Shear, IInkTransform::Shear, Shear, Shear method [Tablet PC], Shear method [Tablet PC],IInkTransform interface, msinkaut/IInkTransform::Shear, tablet.inktransform_shear
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
 - IInkTransform.Shear
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTransform::Shear


## -description



Adjusts the shear of the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> by the specified horizontal and vertical factors.




## -parameters




### -param HorizontalComponent [in]

 The horizontal factor of the shear.


### -param VerticalComponent [in]

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

<div class="alert"><b>Note</b>  When both parameters are nonzero, the results are difficult to predict. For example, if both factors are 1, the transformation squeezes the entire plane to a single line.</div>
<div> </div>



## -see-also




<a href="tablet.iinktransform">IInkTransform</a>



<a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform Class</a>
 

 

