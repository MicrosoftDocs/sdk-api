---
UID: NF:d2d1svg.ID2D1SvgDocument.CreatePathData
title: ID2D1SvgDocument::CreatePathData (d2d1svg.h)
description: Creates a path data object which can be used to set a 'd' attribute on a 'path' element.
helpviewer_keywords: ["CreatePathData","CreatePathData method [Direct2D]","CreatePathData method [Direct2D]","ID2D1SvgDocument interface","ID2D1SvgDocument interface [Direct2D]","CreatePathData method","ID2D1SvgDocument.CreatePathData","ID2D1SvgDocument::CreatePathData","d2d1svg/ID2D1SvgDocument::CreatePathData","direct2d.id2d1svgdocument_createpathdata"]
old-location: direct2d\id2d1svgdocument_createpathdata.htm
tech.root: Direct2D
ms.assetid: 3BF28252-AC33-4B16-9A72-2838006C4A21
ms.date: 12/05/2018
ms.keywords: CreatePathData, CreatePathData method [Direct2D], CreatePathData method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreatePathData method, ID2D1SvgDocument.CreatePathData, ID2D1SvgDocument::CreatePathData, d2d1svg/ID2D1SvgDocument::CreatePathData, direct2d.id2d1svgdocument_createpathdata
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
 - ID2D1SvgDocument::CreatePathData
 - d2d1svg/ID2D1SvgDocument::CreatePathData
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
 - ID2D1SvgDocument.CreatePathData
---

# ID2D1SvgDocument::CreatePathData


## -description

Creates a path data object which can be used to set a 'd' attribute on a 'path' element.

## -parameters

### -param segmentData [in, optional]

Type: <b>const FLOAT*</b>

An array of segment data.

### -param segmentDataCount

Type: <b>UINT32</b>

Number of items in segmentData.

### -param commands [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_path_command">D2D1_SVG_PATH_COMMAND</a>*</b>

An array of path commands.

### -param commandsCount

Type: <b>UINT32</b>

The number of items in commands.

### -param pathData [out]

Type: <b>ID2D1SvgPathData**</b>

When this method completes, this points to the created path data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>