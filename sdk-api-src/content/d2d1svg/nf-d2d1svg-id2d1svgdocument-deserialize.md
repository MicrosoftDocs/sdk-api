---
UID: NF:d2d1svg.ID2D1SvgDocument.Deserialize
title: ID2D1SvgDocument::Deserialize (d2d1svg.h)
description: Deserializes a subtree from the stream. The stream must have only one root element, but that root element need not be an 'svg' element. The output element is not inserted into this document tree.
helpviewer_keywords: ["Deserialize","Deserialize method [Direct2D]","Deserialize method [Direct2D]","ID2D1SvgDocument interface","ID2D1SvgDocument interface [Direct2D]","Deserialize method","ID2D1SvgDocument.Deserialize","ID2D1SvgDocument::Deserialize","d2d1svg/ID2D1SvgDocument::Deserialize","direct2d.id2d1svgdocument_deserialize"]
old-location: direct2d\id2d1svgdocument_deserialize.htm
tech.root: Direct2D
ms.assetid: 576A1D80-3FB5-4495-85CD-2E1DDBCA1C99
ms.date: 12/05/2018
ms.keywords: Deserialize, Deserialize method [Direct2D], Deserialize method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],Deserialize method, ID2D1SvgDocument.Deserialize, ID2D1SvgDocument::Deserialize, d2d1svg/ID2D1SvgDocument::Deserialize, direct2d.id2d1svgdocument_deserialize
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
 - ID2D1SvgDocument::Deserialize
 - d2d1svg/ID2D1SvgDocument::Deserialize
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
 - ID2D1SvgDocument.Deserialize
---

# ID2D1SvgDocument::Deserialize


## -description

Deserializes a subtree from the stream. The stream must have only one root element, but that root element need not be an 'svg' element.
          The output element is not inserted into this document tree.

## -parameters

### -param inputXmlStream [in]

Type: <b>IStream*</b>

An input stream containing the SVG XML subtree.

### -param subtree [out]

Type: <b>ID2D1SvgElement**</b>

The root of the subtree.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>