---
UID: NF:d2d1_3.ID2D1DeviceContext5.CreateSvgDocument
title: ID2D1DeviceContext5::CreateSvgDocument (d2d1_3.h)
description: Creates an SVG document from a stream.
helpviewer_keywords: ["CreateSvgDocument","CreateSvgDocument method [Direct2D]","CreateSvgDocument method [Direct2D]","ID2D1DeviceContext5 interface","ID2D1DeviceContext5 interface [Direct2D]","CreateSvgDocument method","ID2D1DeviceContext5.CreateSvgDocument","ID2D1DeviceContext5::CreateSvgDocument","d2d1_3/ID2D1DeviceContext5::CreateSvgDocument","direct2d.id2d1devicecontext5_createsvgdocument"]
old-location: direct2d\id2d1devicecontext5_createsvgdocument.htm
tech.root: Direct2D
ms.assetid: B7965388-EFF0-40B4-AE00-3AB28DEA800B
ms.date: 12/05/2018
ms.keywords: CreateSvgDocument, CreateSvgDocument method [Direct2D], CreateSvgDocument method [Direct2D],ID2D1DeviceContext5 interface, ID2D1DeviceContext5 interface [Direct2D],CreateSvgDocument method, ID2D1DeviceContext5.CreateSvgDocument, ID2D1DeviceContext5::CreateSvgDocument, d2d1_3/ID2D1DeviceContext5::CreateSvgDocument, direct2d.id2d1devicecontext5_createsvgdocument
req.header: d2d1_3.h
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext5::CreateSvgDocument
 - d2d1_3/ID2D1DeviceContext5::CreateSvgDocument
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext5.CreateSvgDocument
---

# ID2D1DeviceContext5::CreateSvgDocument


## -description

Creates an SVG document from a stream.

## -parameters

### -param inputXmlStream [in, optional]

Type: <b>IStream*</b>

An input stream containing the SVG XML document. If null, an empty document is created.

### -param viewportSize

Type: <b>D2D1_SIZE_F</b>

Size of the initial viewport of the document.

### -param svgDocument [out]

Type: <b>ID2D1SvgDocument**</b>

When this method returns, contains a pointer to the created SVG document.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext5">ID2D1DeviceContext5</a>