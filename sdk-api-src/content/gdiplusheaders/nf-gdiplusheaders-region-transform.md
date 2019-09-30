---
UID: NF:gdiplusheaders.Region.Transform
title: Region::Transform (gdiplusheaders.h)
author: windows-sdk-content
description: The Region::Transform method transforms this region by multiplying each of its data points by a specified matrix.
old-location: gdiplus\_gdiplus_CLASS_Region_Transform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\transform_64matrix.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Region class [GDI+],Transform method, Region.Transform, Region::Transform, Transform, Transform method [GDI+], Transform method [GDI+],Region class, _gdiplus_CLASS_Region_Transform_matrix_, gdiplus._gdiplus_CLASS_Region_Transform_matrix_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/Region.Transform"
req.header: gdiplusheaders.h
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
 - Region.Transform
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Region::Transform


## -description


The <b>Region::Transform</b> method transforms this region by multiplying each of its data points by a specified matrix.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a matrix that specifies the transformation. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-translate(inint_inint)">Region::Translate Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

