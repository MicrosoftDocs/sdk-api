---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0008
title: ValueMapType (pla.h)
description: Defines the type of the value.
old-location: pla\valuemaptype.htm
tech.root: PLA
ms.assetid: cc217b3b-389a-4d15-b47d-456778f3eaec
ms.date: 12/05/2018
ms.keywords: ValueMapType, ValueMapType enumeration [PLA], base.valuemaptype, pla.valuemaptype, pla/ValueMapType, pla/plaFlag, pla/plaFlagArray, pla/plaIndex, pla/plaValidation, plaFlag, plaFlagArray, plaIndex, plaValidation
ms.topic: enum
f1_keywords:
- pla/ValueMapType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Pla.h
api_name:
- ValueMapType
targetos: Windows
req.typenames: ValueMapType
req.redist: 
ms.custom: 19H1
---

# ValueMapType enumeration


## -description


Defines the type of the value.


## -enum-fields




### -field plaIndex

Only one item in the collection can be enabled. The enabled item is the value of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property. If more than one item is enabled, the first enabled item is used as the value.


### -field plaFlag

One or more items in the collection can be enabled. An item in the collection represents a single bit flag. The enabled items in the collection are combined  with the <b>OR</b> operator to become the value of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a>.


### -field plaFlagArray

The collection contains a list of Event Tracing for Windows extended flags (see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_properties">ITraceDataProvider::Properties</a> property).


### -field plaValidation

The collection contains a list of HRESULT values returned by the validation process.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_valuemaptype">IValueMap::ValueMapType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_valuemaptype">IValueMapItem::ValueMapType</a>
 

 

