---
UID: NF:gdipluspen.Pen.GetTransform
title: Pen::GetTransform
author: windows-sdk-content
description: The Pen::GetTransform method gets the world transformation matrix currently set for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\gettransform_97matrix.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],Pen class, Pen class [GDI+],GetTransform method, Pen.GetTransform, Pen::GetTransform, _gdiplus_CLASS_Pen_GetTransform_matrix_, gdiplus._gdiplus_CLASS_Pen_GetTransform_matrix_
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::GetTransform


## -description


The <b>Pen::GetTransform</b> method gets the world transformation matrix currently set for this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535037(v=VS.85).aspx">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535038(v=VS.85).aspx">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535039(v=VS.85).aspx">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535040(v=VS.85).aspx">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535056(v=VS.85).aspx">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

