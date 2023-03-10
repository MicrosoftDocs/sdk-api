---
UID: NF:d2d1svg.ID2D1SvgElement.GetSpecifiedAttributeCount
title: ID2D1SvgElement::GetSpecifiedAttributeCount (d2d1svg.h)
description: Returns the number of specified attributes on this element.
helpviewer_keywords: ["GetSpecifiedAttributeCount","GetSpecifiedAttributeCount method [Direct2D]","GetSpecifiedAttributeCount method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetSpecifiedAttributeCount method","ID2D1SvgElement.GetSpecifiedAttributeCount","ID2D1SvgElement::GetSpecifiedAttributeCount","d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeCount","direct2d.id2d1svgelement_getspecifiedattributecount"]
old-location: direct2d\id2d1svgelement_getspecifiedattributecount.htm
tech.root: Direct2D
ms.assetid: DB683CA6-57B5-4B13-9EB3-269DDCA94667
ms.date: 12/05/2018
ms.keywords: GetSpecifiedAttributeCount, GetSpecifiedAttributeCount method [Direct2D], GetSpecifiedAttributeCount method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetSpecifiedAttributeCount method, ID2D1SvgElement.GetSpecifiedAttributeCount, ID2D1SvgElement::GetSpecifiedAttributeCount, d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeCount, direct2d.id2d1svgelement_getspecifiedattributecount
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
 - ID2D1SvgElement::GetSpecifiedAttributeCount
 - d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeCount
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
 - ID2D1SvgElement.GetSpecifiedAttributeCount
---

# ID2D1SvgElement::GetSpecifiedAttributeCount


## -description

Returns the number of specified attributes on this element. Attributes are only considered specified if they are explicitly set on the element or present within an inline style. 
        Properties that receive their value through CSS inheritance are not considered specified. 
        An attribute can become specified if it is set through a method call. 
        It can become unspecified if it is removed via <a href="/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgelement-removeattribute">RemoveAttribute</a>.



## -returns

Type: <b>UINT32</b>

Returns the number of specified attributes on this element.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>
