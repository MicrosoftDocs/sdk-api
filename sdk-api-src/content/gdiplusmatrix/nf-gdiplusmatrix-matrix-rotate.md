---
UID: NF:gdiplusmatrix.Matrix.Rotate
title: Matrix::Rotate (gdiplusmatrix.h)
author: windows-sdk-content
description: The Matrix::Rotate method updates this matrix with the product of itself and a rotation matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Rotate_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\rotate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Matrix class [GDI+],Rotate method, Matrix.Rotate, Matrix::Rotate, Rotate, Rotate method [GDI+], Rotate method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Rotate_angle_order_, gdiplus._gdiplus_CLASS_Matrix_Rotate_angle_order_
ms.topic: method
req.header: gdiplusmatrix.h
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
 - Matrix.Rotate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::Rotate


## -description


The <b>Matrix::Rotate</b> method updates this matrix with the product of itself and a rotation matrix.


## -parameters




### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle of rotation in degrees. Positive values specify clockwise rotation. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the rotation matrix is on the left, and MatrixOrderAppend specifies that the rotation matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536395(v=VS.85).aspx">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535308(v=VS.85).aspx">Matrix::Multiply</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535313(v=VS.85).aspx">Matrix::RotateAt</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535314(v=VS.85).aspx">Matrix::Scale</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535316(v=VS.85).aspx">Matrix::Shear</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535317(v=VS.85).aspx">Matrix::Translate</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

