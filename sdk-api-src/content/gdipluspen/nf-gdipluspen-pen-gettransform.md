---
UID: NF:gdipluspen.Pen.GetTransform
title: Pen::GetTransform
author: windows-sdk-content
description: The Pen::GetTransform method gets the world transformation matrix currently set for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\gettransform_97matrix.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],Pen class, Pen class [GDI+],GetTransform method, Pen.GetTransform, Pen::GetTransform, _gdiplus_CLASS_Pen_GetTransform_matrix_, gdiplus._gdiplus_CLASS_Pen_GetTransform_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
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
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/29ea3ff0-0cfa-4f4c-a292-824fdd0705ce">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/2a473f75-ad8c-4616-98fd-d87946409bb1">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/c88b622c-3c9d-4640-96f5-0bccddd6f412">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/0605fcdb-bb04-46dd-8818-9d524a1d90d1">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/e6a5a579-98a6-43dd-a6b2-882c6a449046">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

