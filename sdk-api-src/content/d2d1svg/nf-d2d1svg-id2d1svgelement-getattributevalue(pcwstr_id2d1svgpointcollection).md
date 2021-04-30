---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValue(PCWSTR,ID2D1SvgPointCollection)
title: ID2D1SvgElement::GetAttributeValue(PCWSTR,ID2D1SvgPointCollection) (d2d1svg.h)
description: Gets an attribute of this element as points. This method can be used to get the value of the points attribute on a polygon or polyline element.
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Direct2D]","GetAttributeValue method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetAttributeValue method","ID2D1SvgElement.GetAttributeValue","ID2D1SvgElement.GetAttributeValue(PCWSTR","ID2D1SvgPointCollection)","ID2D1SvgElement::GetAttributeValue","ID2D1SvgElement::GetAttributeValue(PCWSTR","ID2D1SvgPointCollection)","d2d1svg/ID2D1SvgElement::GetAttributeValue","direct2d.id2d1svgelement_getattributevalue_20"]
old-location: direct2d\id2d1svgelement_getattributevalue_20.htm
tech.root: Direct2D
ms.assetid: 2EA7A72F-91A1-46BA-A930-A2000C340DB2
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Direct2D], GetAttributeValue method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValue method, ID2D1SvgElement.GetAttributeValue, ID2D1SvgElement.GetAttributeValue(PCWSTR,ID2D1SvgPointCollection), ID2D1SvgElement::GetAttributeValue, ID2D1SvgElement::GetAttributeValue(PCWSTR,ID2D1SvgPointCollection), d2d1svg/ID2D1SvgElement::GetAttributeValue, direct2d.id2d1svgelement_getattributevalue_20
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

# ID2D1SvgElement::GetAttributeValue(PCWSTR,ID2D1SvgPointCollection)


## -description

Gets an attribute of this element as points. This method can be used to get the value of the points attribute on a polygon or polyline element.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.

### -param value

Type: <b>ID2D1SvgPointCollection**</b>

The value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>