---
UID: NF:gdiplusmatrix.Matrix.Matrix(IN const Rect &,IN const Point)
title: Matrix::Matrix(IN const Rect &,IN const Point) (gdiplusmatrix.h)
author: windows-sdk-content
description: Creates a Matrix::Matrix object based on a rectangle and a point.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Matrix_Rect_rect_Point_dstplg_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixconstructors\matrix_44rectamprect_pointdstplg.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Matrix, Matrix class [GDI+],Matrix constructor, Matrix constructor [GDI+], Matrix constructor [GDI+],Matrix class, Matrix.Matrix, Matrix.Matrix(IN const Rect &,IN const Point), Matrix.Matrix(const Rect&,const Point*), Matrix::Matrix, Matrix::Matrix(IN const Rect &,IN const Point), _gdiplus_CLASS_Matrix_Matrix_Rect_rect_Point_dstplg_, gdiplus._gdiplus_CLASS_Matrix_Matrix_Rect_rect_Point_dstplg_
ms.topic: method
f1_keywords: ["gdiplusmatrix/Matrix.Matrix"]
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
ms.custom: 19H1
---

# Matrix::Matrix(IN const Rect &,IN const Point)


## -description


Creates a <b>Matrix::Matrix</b> object based on a rectangle and a point.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object. The <b>X</b> data member of the rectangle specifies the matrix element in row 1, column 1. The <b>Y</b> data member of the rectangle specifies the matrix element in row 1, column 2. The <b>Width</b> data member of the rectangle specifies the matrix element in row 2, column 1. The <b>Height</b> data member of the rectangle specifies the matrix element in row 2, column 2. 


### -param dstplg [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object. The <b>X</b> data member of the point specifies the matrix element in row 3, column 1. The <b>Y</b> data member of the point specifies the matrix element in row 3, column 2. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-class-matrix-constructors">Matrix Constructors</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
 

 

