---
UID: NF:gdiplusmatrix.Matrix.GetLastStatus
title: Matrix::GetLastStatus (gdiplusmatrix.h)
description: The Matrix::GetLastStatus method returns a value that indicates the nature of this Matrix object's most recent method failure.
helpviewer_keywords: ["GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","Matrix class","Matrix class [GDI+]","GetLastStatus method","Matrix.GetLastStatus","Matrix::GetLastStatus","_gdiplus_CLASS_Matrix_GetLastStatus_","gdiplus._gdiplus_CLASS_Matrix_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\getlaststatus_49.htm
ms.date: 12/05/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Matrix class, Matrix class [GDI+],GetLastStatus method, Matrix.GetLastStatus, Matrix::GetLastStatus, _gdiplus_CLASS_Matrix_GetLastStatus_, gdiplus._gdiplus_CLASS_Matrix_GetLastStatus_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Matrix::GetLastStatus
 - gdiplusmatrix/Matrix::GetLastStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Matrix.GetLastStatus
---

# Matrix::GetLastStatus


## -description

The <b>Matrix::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The 
						<b>Matrix::GetLastStatus</b> method returns an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this 
						<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object have failed since the previous call to <b>Matrix::GetLastStatus</b>, then <b>Matrix::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object has failed since the previous call to <b>Matrix::GetLastStatus</b>, then <b>Matrix::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>Matrix::GetLastStatus</b> immediately after constructing a 
				<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object to determine whether the constructor succeeded.

The first time you call the <b>Matrix::GetLastStatus</b> method of a 
				<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Matrix</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
