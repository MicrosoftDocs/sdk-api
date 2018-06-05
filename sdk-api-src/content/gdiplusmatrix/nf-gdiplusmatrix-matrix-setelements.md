---
UID: NF:gdiplusmatrix.Matrix.SetElements
title: Matrix::SetElements
author: windows-sdk-content
description: The Matrix::SetElements method sets the elements of this matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\setelements.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Matrix class [GDI+],SetElements method, Matrix.SetElements, Matrix::SetElements, SetElements, SetElements method [GDI+], SetElements method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_, gdiplus._gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Matrix.SetElements
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
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



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/8d0b7cb7-61cf-4a68-a843-9b68ac74a6b7">Matrix::GetElements</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

