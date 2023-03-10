---
UID: NF:d2d1svg.ID2D1SvgElement.GetDocument
title: ID2D1SvgElement::GetDocument (d2d1svg.h)
description: Gets the document that contains this element.
helpviewer_keywords: ["GetDocument","GetDocument method [Direct2D]","GetDocument method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetDocument method","ID2D1SvgElement.GetDocument","ID2D1SvgElement::GetDocument","d2d1svg/ID2D1SvgElement::GetDocument","direct2d.id2d1svgelement_getdocument"]
old-location: direct2d\id2d1svgelement_getdocument.htm
tech.root: Direct2D
ms.assetid: 87ACD0CD-AF31-4734-80F7-67090154D5D1
ms.date: 12/05/2018
ms.keywords: GetDocument, GetDocument method [Direct2D], GetDocument method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetDocument method, ID2D1SvgElement.GetDocument, ID2D1SvgElement::GetDocument, d2d1svg/ID2D1SvgElement::GetDocument, direct2d.id2d1svgelement_getdocument
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
 - ID2D1SvgElement::GetDocument
 - d2d1svg/ID2D1SvgElement::GetDocument
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
 - ID2D1SvgElement.GetDocument
---

# ID2D1SvgElement::GetDocument


## -description

Gets the document that contains this element.

## -parameters

### -param document [out]

Type: <b>ID2D1SvgDocument**</b>

Outputs the document that contains this element. This argument will be null if the element has been removed from the tree.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>