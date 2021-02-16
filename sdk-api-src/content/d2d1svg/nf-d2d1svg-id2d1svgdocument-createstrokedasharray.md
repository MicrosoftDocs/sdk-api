---
UID: NF:d2d1svg.ID2D1SvgDocument.CreateStrokeDashArray
title: ID2D1SvgDocument::CreateStrokeDashArray (d2d1svg.h)
description: Creates a dash array object which can be used to set the stroke-dasharray property.
helpviewer_keywords: ["CreateStrokeDashArray","CreateStrokeDashArray method [Direct2D]","CreateStrokeDashArray method [Direct2D]","ID2D1SvgDocument interface","ID2D1SvgDocument interface [Direct2D]","CreateStrokeDashArray method","ID2D1SvgDocument.CreateStrokeDashArray","ID2D1SvgDocument::CreateStrokeDashArray","d2d1svg/ID2D1SvgDocument::CreateStrokeDashArray","direct2d.id2d1svgdocument_createstrokedasharray"]
old-location: direct2d\id2d1svgdocument_createstrokedasharray.htm
tech.root: Direct2D
ms.assetid: 559330E4-A0B9-437A-AD83-02C9409B5BE2
ms.date: 12/05/2018
ms.keywords: CreateStrokeDashArray, CreateStrokeDashArray method [Direct2D], CreateStrokeDashArray method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreateStrokeDashArray method, ID2D1SvgDocument.CreateStrokeDashArray, ID2D1SvgDocument::CreateStrokeDashArray, d2d1svg/ID2D1SvgDocument::CreateStrokeDashArray, direct2d.id2d1svgdocument_createstrokedasharray
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
 - ID2D1SvgDocument::CreateStrokeDashArray
 - d2d1svg/ID2D1SvgDocument::CreateStrokeDashArray
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
 - ID2D1SvgDocument.CreateStrokeDashArray
---

# ID2D1SvgDocument::CreateStrokeDashArray


## -description

Creates a dash array object which can be used to set the stroke-dasharray property.

## -parameters

### -param dashes [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length">D2D1_SVG_LENGTH</a>*</b>

An array of dashes.

### -param dashesCount

Type: <b>UINT32</b>

Size of the array in th dashes argument.

### -param strokeDashArray [out]

Type: <b>ID2D1SvgStrokeDashArray**</b>

The created <a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgstrokedasharray">ID2D1SvgStrokeDashArray</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>