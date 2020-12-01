---
UID: NF:d2d1svg.ID2D1SvgElement.InsertChildBefore
title: ID2D1SvgElement::InsertChildBefore (d2d1svg.h)
description: Inserts newChild as a child of this element, before the referenceChild element.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","InsertChildBefore method","ID2D1SvgElement.InsertChildBefore","ID2D1SvgElement::InsertChildBefore","InsertChildBefore","InsertChildBefore method [Direct2D]","InsertChildBefore method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::InsertChildBefore","direct2d.id2d1svgelement_insertchildbefore"]
old-location: direct2d\id2d1svgelement_insertchildbefore.htm
tech.root: Direct2D
ms.assetid: 09BBABC1-0644-473E-A751-C84437941A2B
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],InsertChildBefore method, ID2D1SvgElement.InsertChildBefore, ID2D1SvgElement::InsertChildBefore, InsertChildBefore, InsertChildBefore method [Direct2D], InsertChildBefore method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::InsertChildBefore, direct2d.id2d1svgelement_insertchildbefore
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
 - ID2D1SvgElement::InsertChildBefore
 - d2d1svg/ID2D1SvgElement::InsertChildBefore
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
 - ID2D1SvgElement.InsertChildBefore
---

# ID2D1SvgElement::InsertChildBefore


## -description

Inserts newChild as a child of this element, before the referenceChild element.
         If the newChild element already has a parent, it is removed from this parent as
        part of the insertion.

## -parameters

### -param newChild [in]

Type: <b>ID2D1SvgElement*</b>

The element to be inserted.

### -param referenceChild [in, optional]

Type: <b>ID2D1SvgElement*</b>

The element that the child should be inserted before.
            If referenceChild is null, the newChild is placed as the last child.
            If referenceChild is non-null, it must be an immediate child of this element.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if this element cannot accept children
            of the type of newChild. Returns an error if the newChild is an ancestor of this
            element.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>