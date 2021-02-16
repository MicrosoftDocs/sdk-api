---
UID: NF:d2d1svg.ID2D1SvgElement.SetAttributeValue(PCWSTR,constD2D1_SVG_PRESERVE_ASPECT_RATIO&)
title: ID2D1SvgElement::SetAttributeValue(PCWSTR,const D2D1_SVG_PRESERVE_ASPECT_RATIO &) (d2d1svg.h)
description: Sets an attribute of this element as a preserve aspect ratio value. This method can be used to set the value of a preserveAspectRatio attribute.
helpviewer_keywords: ["ID2D1SvgElement interface [Direct2D]","SetAttributeValue method","ID2D1SvgElement.SetAttributeValue","ID2D1SvgElement.SetAttributeValue(PCWSTR","const D2D1_SVG_PRESERVE_ASPECT_RATIO &)","ID2D1SvgElement::SetAttributeValue","ID2D1SvgElement::SetAttributeValue(PCWSTR","const D2D1_SVG_PRESERVE_ASPECT_RATIO &)","SetAttributeValue","SetAttributeValue method [Direct2D]","SetAttributeValue method [Direct2D]","ID2D1SvgElement interface","d2d1svg/ID2D1SvgElement::SetAttributeValue","direct2d.id2d1svgelement_setattributevalue_15"]
old-location: direct2d\id2d1svgelement_setattributevalue_15.htm
tech.root: Direct2D
ms.assetid: F95B714E-309B-4E6D-99C9-331FB476EC59
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],SetAttributeValue method, ID2D1SvgElement.SetAttributeValue, ID2D1SvgElement.SetAttributeValue(PCWSTR,const D2D1_SVG_PRESERVE_ASPECT_RATIO &), ID2D1SvgElement::SetAttributeValue, ID2D1SvgElement::SetAttributeValue(PCWSTR,const D2D1_SVG_PRESERVE_ASPECT_RATIO &), SetAttributeValue, SetAttributeValue method [Direct2D], SetAttributeValue method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::SetAttributeValue, direct2d.id2d1svgelement_setattributevalue_15
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

# ID2D1SvgElement::SetAttributeValue(PCWSTR,const D2D1_SVG_PRESERVE_ASPECT_RATIO &)


## -description

Sets an attribute of this element as a preserve aspect ratio value. This method can be used to set the value of a preserveAspectRatio attribute.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

Name of the attribute to set.

### -param value [ref]

Type: <b>const <a href="/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio">D2D1_SVG_PRESERVE_ASPECT_RATIO</a></b>

The new value of the attribute.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>