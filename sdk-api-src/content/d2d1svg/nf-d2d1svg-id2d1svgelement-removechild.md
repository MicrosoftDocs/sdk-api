---
UID: NF:d2d1svg.ID2D1SvgElement.RemoveChild
title: ID2D1SvgElement::RemoveChild (d2d1svg.h)
description: Removes the oldChild from the tree. Children of oldChild remain children of oldChild.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","RemoveChild method","ID2D1SvgElement.RemoveChild","ID2D1SvgElement::RemoveChild","RemoveChild","RemoveChild method [Direct2D]","RemoveChild method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::RemoveChild","direct2d.id2d1svgelement_removechild"]
old-location: direct2d\id2d1svgelement_removechild.htm
tech.root: Direct2D
ms.assetid: 986EE898-D377-4DFF-B19E-834D5CD1A4E6
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],RemoveChild method, ID2D1SvgElement.RemoveChild, ID2D1SvgElement::RemoveChild, RemoveChild, RemoveChild method [Direct2D], RemoveChild method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::RemoveChild, direct2d.id2d1svgelement_removechild
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
 - ID2D1SvgElement::RemoveChild
 - d2d1svg/ID2D1SvgElement::RemoveChild
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
 - ID2D1SvgElement.RemoveChild
---

# ID2D1SvgElement::RemoveChild


## -description

Removes the oldChild from the tree. Children of oldChild remain children of oldChild.

## -parameters

### -param oldChild [in]

Type: <b>ID2D1SvgElement*</b>

The child element to be removed. The oldChild element must be an immediate child of this element.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>