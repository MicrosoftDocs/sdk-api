---
UID: NF:gdiplusmatrix.Matrix.Multiply
title: Matrix::Multiply
author: windows-sdk-content
description: The Matrix::Multiply method updates this matrix with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Multiply_matrix_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\multiply.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Matrix class [GDI+],Multiply method, Matrix.Multiply, Matrix::Multiply, Multiply, Multiply method [GDI+], Multiply method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Multiply_matrix_order_, gdiplus._gdiplus_CLASS_Matrix_Multiply_matrix_order_
ms.prod: windows
ms.technology: windows-sdk
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
 - Matrix.Multiply
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Matrix::Multiply


## -description


The <b>Matrix::Multiply</b> method updates this matrix with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a matrix that will be multiplied by this matrix. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the passed matrix is on the left, and MatrixOrderAppend specifies that the passed matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/ms536395(v=VS.85).aspx">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/library/ms535312(v=VS.85).aspx">Matrix::Rotate</a>



<a href="https://msdn.microsoft.com/library/ms535313(v=VS.85).aspx">Matrix::RotateAt</a>



<a href="https://msdn.microsoft.com/library/ms535314(v=VS.85).aspx">Matrix::Scale</a>



<a href="https://msdn.microsoft.com/library/ms535316(v=VS.85).aspx">Matrix::Shear</a>



<a href="https://msdn.microsoft.com/library/ms535317(v=VS.85).aspx">Matrix::Translate</a>



<a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

