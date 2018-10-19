---
UID: NF:gdipluspen.Pen.RotateTransform
title: Pen::RotateTransform
author: windows-sdk-content
description: The Pen::RotateTransform method updates the world transformation matrix of this Pen object with the product of itself and a rotation matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_RotateTransform_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\rotatetransform_45angle_order.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: Pen class [GDI+],RotateTransform method, Pen.RotateTransform, Pen::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_Pen_RotateTransform_angle_order_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.RotateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::RotateTransform


## -description


The <b>Pen::RotateTransform</b> method updates the world transformation matrix of this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object with the product of itself and a rotation matrix.


## -parameters




### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle of rotation in degrees. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the rotation matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the rotation matrix is on the right. The default value is <b>MatrixOrderPrepend</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/b62b1734-119a-4a65-854b-261674a02378">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/29ea3ff0-0cfa-4f4c-a292-824fdd0705ce">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/2a473f75-ad8c-4616-98fd-d87946409bb1">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/0605fcdb-bb04-46dd-8818-9d524a1d90d1">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/e6a5a579-98a6-43dd-a6b2-882c6a449046">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

