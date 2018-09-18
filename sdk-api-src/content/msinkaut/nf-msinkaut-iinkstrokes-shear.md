---
UID: NF:msinkaut.IInkStrokes.Shear
title: IInkStrokes::Shear
author: windows-sdk-content
description: Shears the ink in the stroke or strokes by the specified horizontal and vertical factors.
old-location: tablet\inkstrokes_shear.htm
tech.root: tablet
ms.assetid: 2ae8cf5a-b113-46e8-b8c2-6605f017f826
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 887dd883-1a24-4a78-8f08-f4cd45bf4840, IInkStrokes interface [Tablet PC],Shear method, IInkStrokes.Shear, IInkStrokes::Shear, Shear, Shear method [Tablet PC], Shear method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::Shear, tablet.inkstrokes_shear
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
 - IInkStrokes.Shear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokes::Shear


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




<a href="https://msdn.microsoft.com/496234C1-C20B-46FE-A9BB-4B90C14FEB46">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

