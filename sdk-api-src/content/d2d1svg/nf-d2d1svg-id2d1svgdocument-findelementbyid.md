---
UID: NF:d2d1svg.ID2D1SvgDocument.FindElementById
title: ID2D1SvgDocument::FindElementById (d2d1svg.h)
description: Gets the SVG element with the specified ID.
helpviewer_keywords: ["FindElementById","FindElementById method [Direct2D]","FindElementById method [Direct2D]","ID2D1SvgDocument interface","ID2D1SvgDocument interface [Direct2D]","FindElementById method","ID2D1SvgDocument.FindElementById","ID2D1SvgDocument::FindElementById","d2d1svg/ID2D1SvgDocument::FindElementById","direct2d.id2d1svgdocument_findelementbyid"]
old-location: direct2d\id2d1svgdocument_findelementbyid.htm
tech.root: Direct2D
ms.assetid: B4E4EE0E-0A2B-479A-B101-AC9DF8546A4F
ms.date: 12/05/2018
ms.keywords: FindElementById, FindElementById method [Direct2D], FindElementById method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],FindElementById method, ID2D1SvgDocument.FindElementById, ID2D1SvgDocument::FindElementById, d2d1svg/ID2D1SvgDocument::FindElementById, direct2d.id2d1svgdocument_findelementbyid
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
 - ID2D1SvgDocument::FindElementById
 - d2d1svg/ID2D1SvgDocument::FindElementById
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
 - ID2D1SvgDocument.FindElementById
---

# ID2D1SvgDocument::FindElementById


## -description

Gets the SVG element with the specified ID.

## -parameters

### -param id [in]

Type: <b>PCWSTR</b>

ID of the element to retrieve.

### -param svgElement

Type: <b>ID2D1SvgElement**</b>

The element matching the specified ID. If the element cannot be found, the returned element will be null.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>