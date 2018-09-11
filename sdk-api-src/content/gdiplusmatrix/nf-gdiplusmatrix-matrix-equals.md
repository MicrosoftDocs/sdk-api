---
UID: NF:gdiplusmatrix.Matrix.Equals
title: Matrix::Equals
author: windows-sdk-content
description: The Matrix::Equals method determines whether the elements of this matrix are equal to the elements of another matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Equals_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\equals.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],Matrix class, Matrix class [GDI+],Equals method, Matrix.Equals, Matrix::Equals, _gdiplus_CLASS_Matrix_Equals_matrix_, gdiplus._gdiplus_CLASS_Matrix_Equals_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Matrix.Equals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::Equals


## -description


The <b>Matrix::Equals</b> method determines whether the elements of this matrix are equal to the elements of another matrix.


## -parameters




### -param matrix [in]

Type: <b>const Matrix*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that is compared with this 
					<b>Matrix</b> object. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the elements of the two matrices are the same, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536395(v=VS.85).aspx">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

