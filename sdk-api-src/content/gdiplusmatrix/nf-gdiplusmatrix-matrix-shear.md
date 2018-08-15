---
UID: NF:gdiplusmatrix.Matrix.Shear
title: Matrix::Shear
author: windows-sdk-content
description: The Matrix::Shear method updates this matrix with the product of itself and a shearing matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\shear.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Matrix class [GDI+],Shear method, Matrix.Shear, Matrix::Shear, Shear, Shear method [GDI+], Shear method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_, gdiplus._gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusmatrix.h
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Matrix.Shear
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Matrix::Shear


## -description


The <b>Matrix::Shear</b> method updates this matrix with the product of itself and a shearing matrix.


## -parameters




### -param shearX [in]

Type: <b>REAL</b>

Real number that specifies the horizontal shear factor. 


### -param shearY [in]

Type: <b>REAL</b>

Real number that specifies the vertical shear factor. 


### -param order [in]

Type: <b>REAL</b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the shearing matrix is on the left, and MatrixOrderAppend specifies that the shearing matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the Status enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536395(v=VS.85).aspx">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535308(v=VS.85).aspx">Matrix::Multiply</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535312(v=VS.85).aspx">Matrix::Rotate</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535313(v=VS.85).aspx">Matrix::RotateAt</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535314(v=VS.85).aspx">Matrix::Scale</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535317(v=VS.85).aspx">Matrix::Translate</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

