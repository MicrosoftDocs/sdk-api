---
UID: NF:pla.IValueMap.get_Value
title: IValueMap::get_Value (pla.h)
description: Retrieves or sets the value of the collection. (Get)
helpviewer_keywords: ["IValueMap interface [PLA]","Value property","IValueMap.Value","IValueMap.get_Value","IValueMap::Value","IValueMap::get_Value","IValueMap::put_Value","Value property [PLA]","Value property [PLA]","IValueMap interface","base.ivaluemap_value","get_Value","pla.ivaluemap_value","pla/IValueMap::Value","pla/IValueMap::get_Value","pla/IValueMap::put_Value"]
old-location: pla\ivaluemap_value.htm
tech.root: PLA
ms.assetid: 9f344845-956e-4254-82e2-e4e00f6a371b
ms.date: 12/05/2018
ms.keywords: IValueMap interface [PLA],Value property, IValueMap.Value, IValueMap.get_Value, IValueMap::Value, IValueMap::get_Value, IValueMap::put_Value, Value property [PLA], Value property [PLA],IValueMap interface, base.ivaluemap_value, get_Value, pla.ivaluemap_value, pla/IValueMap::Value, pla/IValueMap::get_Value, pla/IValueMap::put_Value
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IValueMap::get_Value
 - pla/IValueMap::get_Value
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IValueMap.Value
 - IValueMap.get_Value
 - IValueMap.put_Value
---

# IValueMap::get_Value


## -description

Retrieves or sets the value of the collection.

This property is read/write.

## -parameters

## -remarks

Depending on the value of the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_valuemaptype">IValueMap::ValueMapType</a> property, this value is either one of the values in the collection or the value derived by combining all the item values in the collection with the <b>OR</b> operator.

The variant type is VT_UI8 if the <a href="/windows/win32/api/pla/ne-pla-valuemaptype">ValueMapType</a> enumeration is <b>plaIndex</b>, <b>plaFlag</b> or <b>plaFlagArray</b>.

The variant type is VT_UI4 if the <a href="/windows/win32/api/pla/ne-pla-valuemaptype">ValueMapType</a> enumeration is <b>plaValidation</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_valuemaptype">IValueMap::ValueMapType</a>
