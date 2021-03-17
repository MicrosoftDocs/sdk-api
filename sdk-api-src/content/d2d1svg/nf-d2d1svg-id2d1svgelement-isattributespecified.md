---
UID: NF:d2d1svg.ID2D1SvgElement.IsAttributeSpecified
title: ID2D1SvgElement::IsAttributeSpecified (d2d1svg.h)
description: Returns a boolean indicating if the attribute is explicitly set on the element.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","IsAttributeSpecified method","ID2D1SvgElement.IsAttributeSpecified","ID2D1SvgElement::IsAttributeSpecified","IsAttributeSpecified","IsAttributeSpecified method [Direct2D]","IsAttributeSpecified method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::IsAttributeSpecified","direct2d.id2d1svgelement_isattributespecified"]
old-location: direct2d\id2d1svgelement_isattributespecified.htm
tech.root: Direct2D
ms.assetid: 94B91C4E-B2E5-4E23-B381-5920EA0F8F31
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],IsAttributeSpecified method, ID2D1SvgElement.IsAttributeSpecified, ID2D1SvgElement::IsAttributeSpecified, IsAttributeSpecified, IsAttributeSpecified method [Direct2D], IsAttributeSpecified method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::IsAttributeSpecified, direct2d.id2d1svgelement_isattributespecified
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
 - ID2D1SvgElement::IsAttributeSpecified
 - d2d1svg/ID2D1SvgElement::IsAttributeSpecified
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
 - ID2D1SvgElement.IsAttributeSpecified
---

# ID2D1SvgElement::IsAttributeSpecified


## -description

Returns a boolean indicating if the attribute is explicitly set on the element.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.

### -param inherited [out, optional]

Type: <b>BOOL*</b>

Outputs whether the attribute is set to the inherit value.

## -returns

Type: <b>BOOL</b>

TReturns true if the attribute is explicitly set on the element or if it is present within an inline style. Returns FALSE if the attribute is not a valid
            attribute on this element.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>