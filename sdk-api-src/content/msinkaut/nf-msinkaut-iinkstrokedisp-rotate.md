---
UID: NF:msinkaut.IInkStrokeDisp.Rotate
title: IInkStrokeDisp::Rotate
author: windows-sdk-content
description: Rotates the ink using an angle in degrees around a center point of the rotation.
old-location: tablet\iinkstrokedisp_rotate.htm
tech.root: tablet
ms.assetid: 3b3d5a58-31e8-4d0e-a1c9-25bb36bb8d9c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 3b3d5a58-31e8-4d0e-a1c9-25bb36bb8d9c, IInkStrokeDisp interface [Tablet PC],Rotate method, IInkStrokeDisp.Rotate, IInkStrokeDisp::Rotate, Rotate, Rotate method [Tablet PC], Rotate method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::Rotate, tablet.iinkstrokedisp_rotate
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
 - IInkStrokeDisp.Rotate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokeDisp::Rotate


## -description



Rotates the ink using an angle in degrees around a center point of the rotation.




## -parameters




### -param Degrees [in]

The degrees by which to rotate clockwise.


### -param x [in, optional]

Optional. The x-coordinate of the point in ink space coordinates around which to rotate. Default is the origin. The default value is the origin (0).


### -param y [in, optional]

Optional. The y-coordinate of the point in ink space coordinates around which to rotate. The default value is the origin (0).


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
 




## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

