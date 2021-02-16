---
UID: NS:ocidl.tagCADWORD
title: CADWORD (ocidl.h)
description: Specifies a counted array of values that can be used to obtain the value corresponding to one of the predefined strings for a property.
helpviewer_keywords: ["*LPCADWORD","CADWORD","CADWORD structure [COM]","LPCADWORD","LPCADWORD structure pointer [COM]","_ctrl_CADWORD","com.cadword","ocidl/CADWORD","ocidl/LPCADWORD"]
old-location: com\cadword.htm
tech.root: com
ms.assetid: 4e7f8e1a-53cc-40db-9651-00f5d912e768
ms.date: 12/05/2018
ms.keywords: '*LPCADWORD, CADWORD, CADWORD structure [COM], LPCADWORD, LPCADWORD structure pointer [COM], _ctrl_CADWORD, com.cadword, ocidl/CADWORD, ocidl/LPCADWORD'
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: CADWORD, *LPCADWORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCADWORD
 - ocidl/tagCADWORD
 - LPCADWORD
 - ocidl/LPCADWORD
 - CADWORD
 - ocidl/CADWORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - CADWORD
---

# CADWORD structure


## -description

Specifies a counted array of values that can be used to obtain the value corresponding to one of the predefined strings for a property.

## -struct-fields

### -field cElems

The size of the array pointed to by <b>pElems</b>.

### -field pElems

A pointer to an array of values, each of which can be passed to the <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">IPerPropertyBrowsing::GetPredefinedValue</a> method to obtain the corresponding value for one of the property's predefined strings. This array is allocated by the callee using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and is freed by the caller using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/ns-ocidl-calpolestr">CALPOLESTR</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings">IPerPropertyBrowsing::GetPredefinedStrings</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">IPerPropertyBrowsing::GetPredefinedValue</a>