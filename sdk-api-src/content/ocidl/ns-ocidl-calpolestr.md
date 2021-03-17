---
UID: NS:ocidl.tagCALPOLESTR
title: CALPOLESTR (ocidl.h)
description: Specifies a counted array of strings used to specify the predefined strings that a property can accept.
helpviewer_keywords: ["*LPCALPOLESTR","CALPOLESTR","CALPOLESTR structure [COM]","LPCALPOLESTR","LPCALPOLESTR structure pointer [COM]","_ctrl_CALPOLESTR","com.calpolestr","ocidl/CALPOLESTR","ocidl/LPCALPOLESTR"]
old-location: com\calpolestr.htm
tech.root: com
ms.assetid: 730d5e23-e84a-4629-9b59-492d8536122e
ms.date: 12/05/2018
ms.keywords: '*LPCALPOLESTR, CALPOLESTR, CALPOLESTR structure [COM], LPCALPOLESTR, LPCALPOLESTR structure pointer [COM], _ctrl_CALPOLESTR, com.calpolestr, ocidl/CALPOLESTR, ocidl/LPCALPOLESTR'
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
req.typenames: CALPOLESTR, *LPCALPOLESTR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCALPOLESTR
 - ocidl/tagCALPOLESTR
 - LPCALPOLESTR
 - ocidl/LPCALPOLESTR
 - CALPOLESTR
 - ocidl/CALPOLESTR
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
 - CALPOLESTR
---

# CALPOLESTR structure


## -description

Specifies a counted array of strings used to specify the predefined strings that a property can accept.

## -struct-fields

### -field cElems

The size of the array pointed to by <b>pElems</b>.

### -field pElems

A pointer to an array of <a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">LPOLESTR</a> values, each of which corresponds to an allowable value that a particular property can accept. The caller can use these string values in user interface elements, such as drop-down list boxes. This array, as well as the strings in the array, are allocated by the callee using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and is freed by the caller using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings">IPerPropertyBrowsing::GetPredefinedStrings</a>



<a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">LPOLESTR</a>