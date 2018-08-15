---
UID: NF:gdipluspen.Pen.RotateTransform
title: Pen::RotateTransform
author: windows-sdk-content
description: The Pen::RotateTransform method updates the world transformation matrix of this Pen object with the product of itself and a rotation matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_RotateTransform_angle_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\rotatetransform_45angle_order.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Pen class [GDI+],RotateTransform method, Pen.RotateTransform, Pen::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_Pen_RotateTransform_angle_order_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::RotateTransform


## -description


The <b>Pen::RotateTransform</b> method updates the world transformation matrix of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object with the product of itself and a rotation matrix.


## -parameters




### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle of rotation in degrees. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the rotation matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the rotation matrix is on the right. The default value is <b>MatrixOrderPrepend</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535035(v=VS.85).aspx">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535037(v=VS.85).aspx">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535038(v=VS.85).aspx">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535040(v=VS.85).aspx">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535056(v=VS.85).aspx">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

