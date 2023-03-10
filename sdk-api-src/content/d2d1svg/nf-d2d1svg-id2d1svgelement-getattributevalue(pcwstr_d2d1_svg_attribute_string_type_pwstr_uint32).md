---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PWSTR,UINT32)
title: ID2D1SvgElement::GetAttributeValue (d2d1svg.h)
description: Gets an attribute of this element as a string. (overload 1/2)
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Direct2D]","GetAttributeValue method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetAttributeValue method","ID2D1SvgElement.GetAttributeValue","ID2D1SvgElement::GetAttributeValue","ID2D1SvgElement::GetAttributeValue(PCWSTR","D2D1_SVG_ATTRIBUTE_STRING_TYPE","PWSTR","UINT32)","d2d1svg/ID2D1SvgElement::GetAttributeValue","direct2d.id2d1svgelement_getattributevalue"]
old-location: direct2d\id2d1svgelement_getattributevalue.htm
tech.root: Direct2D
ms.assetid: 3C05DC2D-6B45-4979-8BBC-CD437068B92A
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Direct2D], GetAttributeValue method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValue method, ID2D1SvgElement.GetAttributeValue, ID2D1SvgElement::GetAttributeValue, ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PWSTR,UINT32), d2d1svg/ID2D1SvgElement::GetAttributeValue, direct2d.id2d1svgelement_getattributevalue
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
 - ID2D1SvgElement::GetAttributeValue
 - d2d1svg/ID2D1SvgElement::GetAttributeValue
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
 - ID2D1SvgElement.GetAttributeValue
---

## -description

Gets an attribute of this element as a string.

## -parameters

### -param name

Type: [in] <b>PCWSTR</b>

The name of the attribute.

### -param type

Type: [in] <b><a href="/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_attribute_string_type">D2D1_SVG_ATTRIBUTE_STRING_TYPE</a></b>

The string type.

### -param value

Type: [out] <b>PWSTR</b>

The value of the attribute.

### -param valueCount

Type: [out] <b>UINT32</b>

The number of elements in the returned value.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if the attribute name is not valid on this element. Returns an error if the attribute cannot be expressed as the specified string type.  Returns an error if the attribute is not specified.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>
