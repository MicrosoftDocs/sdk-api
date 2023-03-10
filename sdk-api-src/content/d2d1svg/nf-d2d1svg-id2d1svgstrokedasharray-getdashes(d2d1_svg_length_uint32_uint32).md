---
UID: NF:d2d1svg.ID2D1SvgStrokeDashArray.GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32)
title: ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32) (d2d1svg.h)
description: Gets dashes from the array. (overload 2/2)
helpviewer_keywords: ["GetDashes","GetDashes method [Direct2D]","GetDashes method [Direct2D]","ID2D1SvgStrokeDashArray interface","ID2D1SvgStrokeDashArray interface [Direct2D]","GetDashes method","ID2D1SvgStrokeDashArray.GetDashes","ID2D1SvgStrokeDashArray.GetDashes(D2D1_SVG_LENGTH","UINT32","UINT32)","ID2D1SvgStrokeDashArray::GetDashes","ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH","UINT32","UINT32)","d2d1svg/ID2D1SvgStrokeDashArray::GetDashes","direct2d.id2d1svgstrokedasharray_getdashes_2"]
old-location: direct2d\id2d1svgstrokedasharray_getdashes_2.htm
tech.root: Direct2D
ms.assetid: D439F7ED-608B-4A3B-891E-02A9ABD7C537
ms.date: 12/05/2018
ms.keywords: GetDashes, GetDashes method [Direct2D], GetDashes method [Direct2D],ID2D1SvgStrokeDashArray interface, ID2D1SvgStrokeDashArray interface [Direct2D],GetDashes method, ID2D1SvgStrokeDashArray.GetDashes, ID2D1SvgStrokeDashArray.GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32), ID2D1SvgStrokeDashArray::GetDashes, ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32), d2d1svg/ID2D1SvgStrokeDashArray::GetDashes, direct2d.id2d1svgstrokedasharray_getdashes_2
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Direct2d.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgStrokeDashArray::GetDashes
 - d2d1svg/ID2D1SvgStrokeDashArray::GetDashes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgStrokeDashArray.GetDashes
---

# ID2D1SvgStrokeDashArray::GetDashes(D2D1_SVG_LENGTH,UINT32,UINT32)


## -description

Gets dashes from the array.

## -parameters

### -param dashes [out]

Type: <b><a href="/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length">D2D1_SVG_LENGTH</a>*</b>

Buffer to contain the dashes.

### -param dashesCount

Type: <b>UINT32</b>

The element count of the array in the dashes argument.

### -param startIndex

Type: <b>UINT32</b>

The index of the first dash to retrieve.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgstrokedasharray">ID2D1SvgStrokeDashArray</a>
