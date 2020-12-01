---
UID: NF:d2d1svg.ID2D1SvgElement.RemoveAttribute
title: ID2D1SvgElement::RemoveAttribute (d2d1svg.h)
description: Removes the attribute from this element.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","RemoveAttribute method","ID2D1SvgElement.RemoveAttribute","ID2D1SvgElement::RemoveAttribute","RemoveAttribute","RemoveAttribute method [Direct2D]","RemoveAttribute method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::RemoveAttribute","direct2d.id2d1svgelement_removeattribute"]
old-location: direct2d\id2d1svgelement_removeattribute.htm
tech.root: Direct2D
ms.assetid: 608BB970-CC78-4CF3-BD8C-02DCBBFA287E
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],RemoveAttribute method, ID2D1SvgElement.RemoveAttribute, ID2D1SvgElement::RemoveAttribute, RemoveAttribute, RemoveAttribute method [Direct2D], RemoveAttribute method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::RemoveAttribute, direct2d.id2d1svgelement_removeattribute
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
 - ID2D1SvgElement::RemoveAttribute
 - d2d1svg/ID2D1SvgElement::RemoveAttribute
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
 - ID2D1SvgElement.RemoveAttribute
---

# ID2D1SvgElement::RemoveAttribute


## -description

Removes the attribute from this element.  Also removes this attribute from within
        an inline style if present.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute to remove.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if the attribute name is not valid
            on this element.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>