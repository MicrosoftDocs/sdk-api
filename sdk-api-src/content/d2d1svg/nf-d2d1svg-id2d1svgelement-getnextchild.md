---
UID: NF:d2d1svg.ID2D1SvgElement.GetNextChild
title: ID2D1SvgElement::GetNextChild (d2d1svg.h)
description: Gets the next sibling of the referenceChild element.
helpviewer_keywords: ["GetNextChild","GetNextChild method [Direct2D]","GetNextChild method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetNextChild method","ID2D1SvgElement.GetNextChild","ID2D1SvgElement::GetNextChild","d2d1svg/ID2D1SvgElement::GetNextChild","direct2d.id2d1svgelement_getnextchild"]
old-location: direct2d\id2d1svgelement_getnextchild.htm
tech.root: Direct2D
ms.assetid: 41D48F64-3C90-4CB1-91F5-32FC04042471
ms.date: 12/05/2018
ms.keywords: GetNextChild, GetNextChild method [Direct2D], GetNextChild method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetNextChild method, ID2D1SvgElement.GetNextChild, ID2D1SvgElement::GetNextChild, d2d1svg/ID2D1SvgElement::GetNextChild, direct2d.id2d1svgelement_getnextchild
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
 - ID2D1SvgElement::GetNextChild
 - d2d1svg/ID2D1SvgElement::GetNextChild
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
 - ID2D1SvgElement.GetNextChild
---

# ID2D1SvgElement::GetNextChild


## -description

Gets the next sibling of the referenceChild element.

## -parameters

### -param referenceChild [in]

Type: <b>ID2D1SvgElement*</b>

The referenceChild must be an immediate child of this element.

### -param nextChild

Type: <b>ID2D1SvgElement**</b>

The output nextChild element will be non-null if the referenceChild has a next sibling. If the referenceChild is the last child, the output is null.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>