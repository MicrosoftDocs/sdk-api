---
UID: NF:d2d1svg.ID2D1SvgElement.SetAttributeValue(PCWSTR,D2D1_FILL_MODE)
title: ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_FILL_MODE) (d2d1svg.h)
description: Sets an attribute of this element as a fill mode. This method can be used to set the value of the 'fill-rule' or 'clip-rule' properties.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","SetAttributeValue method","ID2D1SvgElement.SetAttributeValue","ID2D1SvgElement.SetAttributeValue(PCWSTR","D2D1_FILL_MODE)","ID2D1SvgElement::SetAttributeValue","ID2D1SvgElement::SetAttributeValue(PCWSTR","D2D1_FILL_MODE)","SetAttributeValue","SetAttributeValue method [Direct2D]","SetAttributeValue method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::SetAttributeValue","direct2d.id2d1svgelement_setattributevalue_6"]
old-location: direct2d\id2d1svgelement_setattributevalue_6.htm
tech.root: Direct2D
ms.assetid: 49EFE20B-4122-4426-9A47-7572696A59A2
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],SetAttributeValue method, ID2D1SvgElement.SetAttributeValue, ID2D1SvgElement.SetAttributeValue(PCWSTR,D2D1_FILL_MODE), ID2D1SvgElement::SetAttributeValue, ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_FILL_MODE), SetAttributeValue, SetAttributeValue method [Direct2D], SetAttributeValue method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::SetAttributeValue, direct2d.id2d1svgelement_setattributevalue_6
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
 - ID2D1SvgElement::SetAttributeValue
 - d2d1svg/ID2D1SvgElement::SetAttributeValue
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
 - ID2D1SvgElement.SetAttributeValue
---

# ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_FILL_MODE)


## -description

Sets an attribute of this element as a fill mode. This method can be used to set the value of the 'fill-rule' or 'clip-rule' properties.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

Name of the attribute to set.

### -param value

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE</a></b>

The new value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>