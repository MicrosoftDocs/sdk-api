---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValue(PCWSTR,ID2D1SvgPathData)
title: ID2D1SvgElement::GetAttributeValue(PCWSTR,ID2D1SvgPathData) (d2d1svg.h)
description: Gets an attribute of this element as path data. This method can be used to get the value of the d attribute on a path element.
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Direct2D]","GetAttributeValue method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetAttributeValue method","ID2D1SvgElement.GetAttributeValue","ID2D1SvgElement.GetAttributeValue(PCWSTR","ID2D1SvgPathData)","ID2D1SvgElement::GetAttributeValue","ID2D1SvgElement::GetAttributeValue(PCWSTR","ID2D1SvgPathData)","d2d1svg/ID2D1SvgElement::GetAttributeValue","direct2d.id2d1svgelement_getattributevalue_21"]
old-location: direct2d\id2d1svgelement_getattributevalue_21.htm
tech.root: Direct2D
ms.assetid: B30040E1-7EF4-4AF1-A261-2820B398B66E
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Direct2D], GetAttributeValue method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValue method, ID2D1SvgElement.GetAttributeValue, ID2D1SvgElement.GetAttributeValue(PCWSTR,ID2D1SvgPathData), ID2D1SvgElement::GetAttributeValue, ID2D1SvgElement::GetAttributeValue(PCWSTR,ID2D1SvgPathData), d2d1svg/ID2D1SvgElement::GetAttributeValue, direct2d.id2d1svgelement_getattributevalue_21
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

# ID2D1SvgElement::GetAttributeValue(PCWSTR,ID2D1SvgPathData)


## -description

Gets an attribute of this element as path data. This method can be used to get the value of the d attribute on a path element.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.

### -param value

Type: <b>ID2D1SvgPathData**</b>

The value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>