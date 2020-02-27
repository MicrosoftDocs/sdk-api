---
UID: NF:d2d1svg.ID2D1SvgElement.SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,const void,UINT32)
title: ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,const void,UINT32) (d2d1svg.h)
description: Sets an attribute of this element using a POD type.
old-location: direct2d\id2d1svgelement_setattributevalue_2.htm
tech.root: Direct2D
ms.assetid: 8ACAA04E-8ABB-49D1-A6F8-BCCEAD1DA460
ms.date: 12/05/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],SetAttributeValue method, ID2D1SvgElement.SetAttributeValue, ID2D1SvgElement.SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,const void,UINT32), ID2D1SvgElement::SetAttributeValue, ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,const void,UINT32), SetAttributeValue, SetAttributeValue method [Direct2D], SetAttributeValue method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::SetAttributeValue, direct2d.id2d1svgelement_setattributevalue_2
f1_keywords:
- d2d1svg/ID2D1SvgElement.SetAttributeValue
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- direct2d.dll
api_name:
- ID2D1SvgElement.SetAttributeValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,const void,UINT32)


## -description


Sets an attribute of this element using a POD type.


## -parameters




### -param name [in]

Type: <b>PCWSTR</b>

Name of the attribute to set.


### -param type

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_attribute_pod_type">D2D1_SVG_ATTRIBUTE_POD_TYPE</a></b>

The POD type of the attribute.


### -param value [in]

Type: <b>const void*</b>

The new value of the attribute.


### -param valueSizeInBytes

Type: <b>UINT32</b>

The size of the new value in bytes.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if the attribute name is not valid on this element. Returns an error if the attribute
            cannot be expressed as the specified type.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>
 

 

