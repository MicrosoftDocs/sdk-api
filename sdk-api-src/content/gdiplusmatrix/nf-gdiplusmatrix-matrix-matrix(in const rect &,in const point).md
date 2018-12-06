---
UID: NF:gdiplusmatrix.Matrix.Matrix(IN const Rect &,IN const Point)
title: Matrix::Matrix(IN const Rect &,IN const Point)
author: windows-sdk-content
description: Creates a Matrix::Matrix object based on a rectangle and a point.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Matrix_Rect_rect_Point_dstplg_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixconstructors\matrix_44rectamprect_pointdstplg.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Matrix, Matrix class [GDI+],Matrix constructor, Matrix constructor [GDI+], Matrix constructor [GDI+],Matrix class, Matrix.Matrix, Matrix.Matrix(IN const Rect &,IN const Point), Matrix.Matrix(const Rect&,const Point*), Matrix::Matrix, Matrix::Matrix(IN const Rect &,IN const Point), _gdiplus_CLASS_Matrix_Matrix_Rect_rect_Point_dstplg_, gdiplus._gdiplus_CLASS_Matrix_Matrix_Rect_rect_Point_dstplg_
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
 - Matrix.Matrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::Matrix(IN const Rect &,IN const Point)


## -description


Creates a <b>Matrix::Matrix</b> object based on a rectangle and a point.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object. The <b>X</b> data member of the rectangle specifies the matrix element in row 1, column 1. The <b>Y</b> data member of the rectangle specifies the matrix element in row 1, column 2. The <b>Width</b> data member of the rectangle specifies the matrix element in row 2, column 1. The <b>Height</b> data member of the rectangle specifies the matrix element in row 2, column 2. 


### -param dstplg [in]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> object. The <b>X</b> data member of the point specifies the matrix element in row 3, column 1. The <b>Y</b> data member of the point specifies the matrix element in row 3, column 2. 


## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/a1411b9c-69e9-441e-a476-b0eb6ec30bf2">Matrix Constructors</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

