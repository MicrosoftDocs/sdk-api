---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValueLength
title: ID2D1SvgElement::GetAttributeValueLength (d2d1svg.h)
description: Gets the string length of an attribute of this element.
helpviewer_keywords: ["GetAttributeValueLength","GetAttributeValueLength method [Direct2D]","GetAttributeValueLength method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetAttributeValueLength method","ID2D1SvgElement.GetAttributeValueLength","ID2D1SvgElement::GetAttributeValueLength","d2d1svg/ID2D1SvgElement::GetAttributeValueLength","direct2d.id2d1svgelement_getattributevaluelength"]
old-location: direct2d\id2d1svgelement_getattributevaluelength.htm
tech.root: Direct2D
ms.assetid: 2B466C04-7768-4F15-AC68-55A3074499C1
ms.date: 12/05/2018
ms.keywords: GetAttributeValueLength, GetAttributeValueLength method [Direct2D], GetAttributeValueLength method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValueLength method, ID2D1SvgElement.GetAttributeValueLength, ID2D1SvgElement::GetAttributeValueLength, d2d1svg/ID2D1SvgElement::GetAttributeValueLength, direct2d.id2d1svgelement_getattributevaluelength
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
 - ID2D1SvgElement::GetAttributeValueLength
 - d2d1svg/ID2D1SvgElement::GetAttributeValueLength
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
 - ID2D1SvgElement.GetAttributeValueLength
---

# ID2D1SvgElement::GetAttributeValueLength


## -description

Gets the string length of an attribute of this element.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.

### -param type

Type: <b><a href="/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_attribute_string_type">D2D1_SVG_ATTRIBUTE_STRING_TYPE</a></b>

The string type of the attribute.

### -param valueLength [out]

Type: <b>UINT32*</b>

The length of the attribute. The returned string length does not include room for the null terminator.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.
        Returns an error if the attribute is not specified. 
        Returns an error if the attribute name is not valid on this element. 
        Returns an error if the attribute cannot be expressed as the specified string type.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>