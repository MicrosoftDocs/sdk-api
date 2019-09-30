---
UID: NF:gdipluspen.Pen.GetTransform
title: Pen::GetTransform (gdipluspen.h)
author: windows-sdk-content
description: The Pen::GetTransform method gets the world transformation matrix currently set for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\gettransform_97matrix.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],Pen class, Pen class [GDI+],GetTransform method, Pen.GetTransform, Pen::GetTransform, _gdiplus_CLASS_Pen_GetTransform_matrix_, gdiplus._gdiplus_CLASS_Pen_GetTransform_matrix_
ms.topic: method
f1_keywords: 
 - "gdipluspen/Pen.GetTransform"
req.header: gdipluspen.h
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
 - Pen.GetTransform
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Pen::GetTransform


## -description


The <b>Pen::GetTransform</b> method gets the world transformation matrix currently set for this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.


## -parameters




### -param matrix [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-multiplytransform">Pen::MultiplyTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-resettransform">Pen::ResetTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-rotatetransform">Pen::RotateTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-scaletransform">Pen::ScaleTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-settransform">Pen::SetTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
 

 

