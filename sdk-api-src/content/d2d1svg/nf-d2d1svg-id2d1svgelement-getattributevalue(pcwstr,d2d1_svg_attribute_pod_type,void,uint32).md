---
UID: NF:d2d1svg.ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,void,UINT32)
title: ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,void,UINT32)
author: windows-sdk-content
description: Gets an attribute of this element as a POD type.
old-location: direct2d\id2d1svgelement_getattributevalue_2.htm
tech.root: direct2d
ms.assetid: E28EA740-E5A6-4C5F-95DB-D3CF8F8922F8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Direct2D], GetAttributeValue method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetAttributeValue method, ID2D1SvgElement.GetAttributeValue, ID2D1SvgElement.GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,void,UINT32), ID2D1SvgElement::GetAttributeValue, ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,void,UINT32), d2d1svg/ID2D1SvgElement::GetAttributeValue, direct2d.id2d1svgelement_getattributevalue_2
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
 - ID2D1SvgElement.GetAttributeValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::GetAttributeValue(PCWSTR,D2D1_SVG_ATTRIBUTE_POD_TYPE,void,UINT32)


## -description


Gets an attribute of this element as a POD type.


## -parameters




### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute.


### -param type

Type: <b><a href="https://msdn.microsoft.com/B04D5E56-8E59-4907-BEA0-D954A300DAD0">D2D1_SVG_ATTRIBUTE_POD_TYPE</a></b>

The POD type of the value.


### -param value [out]

Type: <b>void*</b>

The value of the attribute.


### -param valueSizeInBytes

Type: <b>UINT32</b>

The size of the value in bytes.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if the
            attribute is not specified. Returns an error if the attribute name is not valid
            on this element. Returns an error if the attribute cannot be expressed as the
            specified POD type.
          




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

