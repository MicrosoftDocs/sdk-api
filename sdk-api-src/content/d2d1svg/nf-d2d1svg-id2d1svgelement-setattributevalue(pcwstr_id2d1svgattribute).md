---
UID: NF:d2d1svg.ID2D1SvgElement.SetAttributeValue(PCWSTR,ID2D1SvgAttribute)
title: ID2D1SvgElement::SetAttributeValue(PCWSTR,ID2D1SvgAttribute) (d2d1svg.h)
description: Sets an attribute of this element using an interface.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","SetAttributeValue method","ID2D1SvgElement.SetAttributeValue","ID2D1SvgElement.SetAttributeValue(PCWSTR","ID2D1SvgAttribute)","ID2D1SvgElement::SetAttributeValue","ID2D1SvgElement::SetAttributeValue(PCWSTR","ID2D1SvgAttribute)","SetAttributeValue","SetAttributeValue method [Direct2D]","SetAttributeValue method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::SetAttributeValue","direct2d.id2d1svgelement_setattributevalue_3"]
old-location: direct2d\id2d1svgelement_setattributevalue_3.htm
tech.root: Direct2D
ms.assetid: 1E4AAA78-6746-4DD8-8BD8-C1AB63A51A9B
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],SetAttributeValue method, ID2D1SvgElement.SetAttributeValue, ID2D1SvgElement.SetAttributeValue(PCWSTR,ID2D1SvgAttribute), ID2D1SvgElement::SetAttributeValue, ID2D1SvgElement::SetAttributeValue(PCWSTR,ID2D1SvgAttribute), SetAttributeValue, SetAttributeValue method [Direct2D], SetAttributeValue method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::SetAttributeValue, direct2d.id2d1svgelement_setattributevalue_3
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

# ID2D1SvgElement::SetAttributeValue(PCWSTR,ID2D1SvgAttribute)


## -description

Sets an attribute of this element using an interface.

A given attribute object may only be set on one element in one attribute location at a time.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

Name of the attribute to set.

### -param value [in]

Type: <b>ID2D1SvgAttribute*</b>

The new value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.    Returns an error if the attribute name is not valid on this element.
            Returns an error if the attribute cannot be expressed as the specified interface type.
            Returns an error if the attribute object is already set on an element.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>