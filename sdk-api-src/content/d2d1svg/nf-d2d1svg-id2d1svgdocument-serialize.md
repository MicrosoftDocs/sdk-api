---
UID: NF:d2d1svg.ID2D1SvgDocument.Serialize
title: ID2D1SvgDocument::Serialize (d2d1svg.h)
description: Serializes an element and its subtree to XML. The output XML is encoded as UTF-8.
helpviewer_keywords: ["ID2D1SvgDocument interface [Direct2D]","Serialize method","ID2D1SvgDocument.Serialize","ID2D1SvgDocument::Serialize","Serialize","Serialize method [Direct2D]","Serialize method [Direct2D]","ID2D1SvgDocument interface","d2d1svg/ID2D1SvgDocument::Serialize","direct2d.id2d1svgdocument_serialize"]
old-location: direct2d\id2d1svgdocument_serialize.htm
tech.root: Direct2D
ms.assetid: 799E975A-F3BF-4832-AE51-DA064E5C698E
ms.date: 12/05/2018
ms.keywords: ID2D1SvgDocument interface [Direct2D],Serialize method, ID2D1SvgDocument.Serialize, ID2D1SvgDocument::Serialize, Serialize, Serialize method [Direct2D], Serialize method [Direct2D],ID2D1SvgDocument interface, d2d1svg/ID2D1SvgDocument::Serialize, direct2d.id2d1svgdocument_serialize
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
 - ID2D1SvgDocument::Serialize
 - d2d1svg/ID2D1SvgDocument::Serialize
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
 - ID2D1SvgDocument.Serialize
---

# ID2D1SvgDocument::Serialize


## -description

Serializes an element and its subtree to XML. The output XML is encoded as UTF-8.

## -parameters

### -param outputXmlStream [in]

Type: <b>IStream*</b>

An output stream to contain the SVG XML subtree.

### -param subtree [in, optional]

Type: <b>ID2D1SvgElement*</b>

The root of the subtree. If null, the entire document is serialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>