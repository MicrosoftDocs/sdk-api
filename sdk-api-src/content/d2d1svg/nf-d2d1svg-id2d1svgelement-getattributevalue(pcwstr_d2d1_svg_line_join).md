---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_SVG_LINE_JOIN)
title: ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_LINE_JOIN) (d2d1svg.h)
description: Gets an attribute of this element as a line join value. This method can be used to get the value of the stroke-linejoin property.
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Direct2D]","GetAttributeValue method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetAttributeValue method","ID2D1SvgElement.GetAttributeValue","ID2D1SvgElement.GetAttributeValue(PCWSTR","D2D1_SVG_LINE_JOIN)","ID2D1SvgElement::GetAttributeValue","ID2D1SvgElement::GetAttributeValue(PCWSTR","D2D1_SVG_LINE_JOIN)","d2d1svg/ID2D1SvgElement::GetAttributeValue","direct2d.id2d1svgelement_getattributevalue_9"]
old-location: direct2d\id2d1svgelement_getattributevalue_9.htm
tech.root: Direct2D
ms.assetid: F7B2E7B0-CCDE-4B37-93F7-5DBA83AE9191
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Direct2D], GetAttributeValue method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValue method, ID2D1SvgElement.GetAttributeValue, ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_SVG_LINE_JOIN), ID2D1SvgElement::GetAttributeValue, ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_LINE_JOIN), d2d1svg/ID2D1SvgElement::GetAttributeValue, direct2d.id2d1svgelement_getattributevalue_9
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

# ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_LINE_JOIN)


## -description

Gets an attribute of this element as a line join value. This method can be used to get the value of the stroke-linejoin property.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.

### -param value [out]

Type: <b><a href="/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_line_join">D2D1_SVG_LINE_JOIN</a>*</b>

The value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>