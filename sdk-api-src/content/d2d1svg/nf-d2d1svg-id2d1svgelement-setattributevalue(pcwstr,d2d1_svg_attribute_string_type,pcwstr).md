---
UID: NF:d2d1svg.ID2D1SvgElement.SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PCWSTR)
title: ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PCWSTR)
author: windows-sdk-content
description: Sets an attribute of this element using a string.
old-location: direct2d\id2d1svgelement_setattributevalue.htm
tech.root: Direct2D
ms.assetid: 56796F1B-5DC2-4E9C-A80E-40EA791E6784
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],SetAttributeValue method, ID2D1SvgElement.SetAttributeValue, ID2D1SvgElement.SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PCWSTR), ID2D1SvgElement::SetAttributeValue, ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PCWSTR), SetAttributeValue, SetAttributeValue method [Direct2D], SetAttributeValue method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::SetAttributeValue, direct2d.id2d1svgelement_setattributevalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::SetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_STRING_TYPE,PCWSTR)


## -description


Sets an attribute of this element using a string. 


## -parameters




### -param name [in]

Type: <b>PCWSTR</b>

Name of the attribute to set.


### -param type

Type: <b><a href="https://msdn.microsoft.com/71991A28-FEA0-42A1-B5D0-DA13BBA77500">D2D1_SVG_ATTRIBUTE_STRING_TYPE</a></b>

The type of the string.


### -param value [in]

Type: <b>PCWSTR</b>

The new value of the attribute.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if the
            attribute name is not valid on this element. Returns an error if the attribute
            cannot be expressed as the specified type.
          




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

