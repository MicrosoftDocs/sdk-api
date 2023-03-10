---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_FILL_MODE)
title: ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_FILL_MODE) (d2d1svg.h)
description: Gets an attribute of this element as a fill mode. This method can be used to get the value of the fill-rule or clip-rule properties.
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Direct2D]","GetAttributeValue method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetAttributeValue method","ID2D1SvgElement.GetAttributeValue","ID2D1SvgElement.GetAttributeValue(PCWSTR","D2D1_FILL_MODE)","ID2D1SvgElement::GetAttributeValue","ID2D1SvgElement::GetAttributeValue(PCWSTR","D2D1_FILL_MODE)","d2d1svg/ID2D1SvgElement::GetAttributeValue","direct2d.id2d1svgelement_getattributevalue_6"]
old-location: direct2d\id2d1svgelement_getattributevalue_6.htm
tech.root: Direct2D
ms.assetid: 26F7B02A-7A2C-4C73-BD30-426579F467AC
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Direct2D], GetAttributeValue method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValue method, ID2D1SvgElement.GetAttributeValue, ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_FILL_MODE), ID2D1SvgElement::GetAttributeValue, ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_FILL_MODE), d2d1svg/ID2D1SvgElement::GetAttributeValue, direct2d.id2d1svgelement_getattributevalue_6
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

# ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_FILL_MODE)


## -description

Gets an attribute of this element as a fill mode. This method can be used to get the value of the fill-rule or clip-rule properties.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.

### -param value [out]

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE</a>*</b>

The value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>