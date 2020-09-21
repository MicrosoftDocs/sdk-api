---
UID: NF:gdiplusheaders.Region.Transform
title: Region::Transform (gdiplusheaders.h)
description: The Region::Transform method transforms this region by multiplying each of its data points by a specified matrix.
helpviewer_keywords: ["Region class [GDI+]","Transform method","Region.Transform","Region::Transform","Transform","Transform method [GDI+]","Transform method [GDI+]","Region class","_gdiplus_CLASS_Region_Transform_matrix_","gdiplus._gdiplus_CLASS_Region_Transform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Transform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\transform_64matrix.htm
ms.date: 12/05/2018
ms.keywords: Region class [GDI+],Transform method, Region.Transform, Region::Transform, Transform, Transform method [GDI+], Transform method [GDI+],Region class, _gdiplus_CLASS_Region_Transform_matrix_, gdiplus._gdiplus_CLASS_Region_Transform_matrix_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Region::Transform
 - gdiplusheaders/Region::Transform
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
 - Region.Transform
---

# Region::Transform


## -description

The <b>Region::Transform</b> method transforms this region by multiplying each of its data points by a specified matrix.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a matrix that specifies the transformation.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-translate(inint_inint)">Region::Translate Methods</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>