---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0008
title: ValueMapType (pla.h)
description: Defines the type of the value.
helpviewer_keywords: ["ValueMapType","ValueMapType enumeration [PLA]","base.valuemaptype","pla.valuemaptype","pla/ValueMapType","pla/plaFlag","pla/plaFlagArray","pla/plaIndex","pla/plaValidation","plaFlag","plaFlagArray","plaIndex","plaValidation"]
old-location: pla\valuemaptype.htm
tech.root: PLA
ms.assetid: cc217b3b-389a-4d15-b47d-456778f3eaec
ms.date: 12/05/2018
ms.keywords: ValueMapType, ValueMapType enumeration [PLA], base.valuemaptype, pla.valuemaptype, pla/ValueMapType, pla/plaFlag, pla/plaFlagArray, pla/plaIndex, pla/plaValidation, plaFlag, plaFlagArray, plaIndex, plaValidation
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ValueMapType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0008
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0008
 - ValueMapType
 - pla/ValueMapType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - ValueMapType
---

# ValueMapType enumeration


## -description

Defines the type of the value.

## -enum-fields

### -field plaIndex:1

Only one item in the collection can be enabled. The enabled item is the value of the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property. If more than one item is enabled, the first enabled item is used as the value.

### -field plaFlag:2

One or more items in the collection can be enabled. An item in the collection represents a single bit flag. The enabled items in the collection are combined  with the <b>OR</b> operator to become the value of <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a>.

### -field plaFlagArray:3

The collection contains a list of Event Tracing for Windows extended flags (see the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_properties">ITraceDataProvider::Properties</a> property).

### -field plaValidation:4

The collection contains a list of HRESULT values returned by the validation process.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_valuemaptype">IValueMap::ValueMapType</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_valuemaptype">IValueMapItem::ValueMapType</a>
