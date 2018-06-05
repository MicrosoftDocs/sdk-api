---
UID: NF:msinkaut.IInkStrokes.Rotate
title: IInkStrokes::Rotate
author: windows-sdk-content
description: Rotates the ink using an angle in degrees around a center point of the rotation.
old-location: tablet\inkstrokes_rotate.htm
old-project: tablet
ms.assetid: d198215d-9504-4c87-addb-63d863a6ede3
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 3b3d5a58-31e8-4d0e-a1c9-25bb36bb8d9c, IInkStrokes interface [Tablet PC],Rotate method, IInkStrokes.Rotate, IInkStrokes::Rotate, Rotate, Rotate method [Tablet PC], Rotate method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::Rotate, tablet.inkstrokes_rotate
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokes.Rotate
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokes::Rotate


## -description



Rotates the ink using an angle in degrees around a center point of the rotation.




## -parameters




### -param Degrees [in]

The degrees by which to rotate clockwise.


### -param x [in, optional]

Optional. The x-coordinate of the point in ink space coordinates around which to rotate. Default is the origin.


### -param y [in, optional]

Optional. The y-coordinate of the point in ink space coordinates around which to rotate. Default is the origin.


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




<a href="tablet.iinkstrokes">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

