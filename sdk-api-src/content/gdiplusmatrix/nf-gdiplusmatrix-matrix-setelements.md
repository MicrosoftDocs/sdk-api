---
UID: NF:gdiplusmatrix.Matrix.SetElements
title: Matrix::SetElements
author: windows-sdk-content
description: The Matrix::SetElements method sets the elements of this matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\setelements.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Matrix class [GDI+],SetElements method, Matrix.SetElements, Matrix::SetElements, SetElements, SetElements method [GDI+], SetElements method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_, gdiplus._gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_
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
 - Matrix.SetElements
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::SetElements


## -description


The <b>Matrix::SetElements</b> method sets the elements of this matrix.


## -parameters




### -param m11 [in]

Type: <b>REAL</b>

Real number that specifies the element in the first row, first column. 


### -param m12 [in]

Type: <b>REAL</b>

Real number that specifies the element in the first row, second column. 


### -param m21 [in]

Type: <b>REAL</b>

Real number that specifies the element in the second row, first column. 


### -param m22 [in]

Type: <b>REAL</b>

Real number that specifies the element in the second row, second column. 


### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the element in the third row, first column. 


### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the element in the third row, second column. 


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



<a href="https://msdn.microsoft.com/en-us/library/ms535301(v=VS.85).aspx">Matrix::GetElements</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

