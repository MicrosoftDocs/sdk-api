---
UID: NF:d2d1svg.ID2D1SvgElement.GetPreviousChild
title: ID2D1SvgElement::GetPreviousChild (d2d1svg.h)
description: Gets the previous sibling of the referenceChild element.
helpviewer_keywords: ["GetPreviousChild","GetPreviousChild method [Direct2D]","GetPreviousChild method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetPreviousChild method","ID2D1SvgElement.GetPreviousChild","ID2D1SvgElement::GetPreviousChild","d2d1svg/ID2D1SvgElement::GetPreviousChild","direct2d.id2d1svgelement_getpreviouschild"]
old-location: direct2d\id2d1svgelement_getpreviouschild.htm
tech.root: Direct2D
ms.assetid: CE4334D8-7A96-464A-BE57-A7B226221FC3
ms.date: 12/05/2018
ms.keywords: GetPreviousChild, GetPreviousChild method [Direct2D], GetPreviousChild method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetPreviousChild method, ID2D1SvgElement.GetPreviousChild, ID2D1SvgElement::GetPreviousChild, d2d1svg/ID2D1SvgElement::GetPreviousChild, direct2d.id2d1svgelement_getpreviouschild
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
 - ID2D1SvgElement::GetPreviousChild
 - d2d1svg/ID2D1SvgElement::GetPreviousChild
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
 - ID2D1SvgElement.GetPreviousChild
---

# ID2D1SvgElement::GetPreviousChild


## -description

Gets the previous sibling of the referenceChild element.

## -parameters

### -param referenceChild [in]

Type: <b>ID2D1SvgElement*</b>

The referenceChild must be an immediate child of this element.

### -param previousChild

Type: <b>ID2D1SvgElement**</b>

The output previousChild element will be non-null if the referenceChild has a previous sibling. If the referenceChild is the first child, the output is null.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>