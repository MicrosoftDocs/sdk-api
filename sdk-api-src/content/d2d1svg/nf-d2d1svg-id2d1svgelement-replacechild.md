---
UID: NF:d2d1svg.ID2D1SvgElement.ReplaceChild
title: ID2D1SvgElement::ReplaceChild (d2d1svg.h)
description: Replaces the oldChild element with the newChild.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","ReplaceChild method","ID2D1SvgElement.ReplaceChild","ID2D1SvgElement::ReplaceChild","ReplaceChild","ReplaceChild method [Direct2D]","ReplaceChild method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::ReplaceChild","direct2d.id2d1svgelement_replacechild"]
old-location: direct2d\id2d1svgelement_replacechild.htm
tech.root: Direct2D
ms.assetid: BEF74F58-D218-46CA-AE02-F15DDAC48FB4
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],ReplaceChild method, ID2D1SvgElement.ReplaceChild, ID2D1SvgElement::ReplaceChild, ReplaceChild, ReplaceChild method [Direct2D], ReplaceChild method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::ReplaceChild, direct2d.id2d1svgelement_replacechild
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
 - ID2D1SvgElement::ReplaceChild
 - d2d1svg/ID2D1SvgElement::ReplaceChild
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
 - ID2D1SvgElement.ReplaceChild
---

# ID2D1SvgElement::ReplaceChild


## -description

Replaces the oldChild element with the newChild. This operation removes the oldChild from the tree.
        If the newChild element already has a parent, it is removed from this parent as part of the replace operation.

## -parameters

### -param newChild [in]

Type: <b>ID2D1SvgElement*</b>

The element to be inserted.

### -param oldChild [in]

Type: <b>ID2D1SvgElement*</b>

The child element to be replaced. The oldChild element must be an immediate child of this element.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if
            this element cannot accept children of the type of newChild. Returns an error if
            the newChild is an ancestor of this element.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>