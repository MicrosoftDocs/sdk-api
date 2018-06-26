---
UID: NF:msinkaut.IInkTransform.Rotate
title: IInkTransform::Rotate
author: windows-sdk-content
description: Changes the amount, measured in degrees, to change the rotation factor of the InkTransform object and optionally the center point of the rotation.
old-location: tablet\inktransform_rotate.htm
old-project: tablet
ms.assetid: 17d7e4b0-ccde-4ad9-9bdc-0f6a72ee762e
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: 17d7e4b0-ccde-4ad9-9bdc-0f6a72ee762e, IInkTransform interface [Tablet PC],Rotate method, IInkTransform.Rotate, IInkTransform::Rotate, Rotate, Rotate method [Tablet PC], Rotate method [Tablet PC],IInkTransform interface, msinkaut/IInkTransform::Rotate, tablet.inktransform_rotate
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
 - IInkTransform.Rotate
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTransform::Rotate


## -description



Changes the amount, measured in degrees, to change the rotation factor of the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object and optionally the center point of the rotation.




## -parameters




### -param Degrees [in]

The degrees by which to rotate clockwise. Without the optional x and y arguments, rotation takes place around the origin point, which by default is the upper left corner of the ink collection area to which the transform is applied.


### -param x [in, optional]

Optional. The x-coordinate of the point in ink space coordinates around which rotation occurs. The default value is 0.


### -param y [in, optional]

Optional. The y-coordinate of the point in ink space coordinates around which rotation occurs. The default value is 0.


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



The center point defaults to the origin.




## -see-also




<a href="tablet.iinktransform">IInkTransform</a>



<a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform Class</a>
 

 

