---
UID: NS:ocidl.tagCAUUID
title: CAUUID (ocidl.h)
author: windows-sdk-content
description: Specifies a counted array of UUID or GUID types used to receive an array of CLSIDs for the property pages that the object wants to display.
old-location: com\cauuid.htm
tech.root: com
ms.assetid: 23b991fb-9494-4d3b-83df-986739beaa14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPCAUUID, CAUUID, CAUUID structure [COM], LPCAUUID, LPCAUUID structure pointer [COM], _ctrl_CAUUID, com.cauuid, ocidl/CAUUID, ocidl/LPCAUUID"
ms.topic: struct
f1_keywords: 
 - "ocidl/CAUUID"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - CAUUID
targetos: Windows
req.typenames: CAUUID, *LPCAUUID
req.redist: 
ms.custom: 19H1
---

# CAUUID structure


## -description


Specifies a counted array of UUID or GUID types used to receive an array of CLSIDs for the property pages that the object wants to display.


## -struct-fields




### -field cElems

The size of the array pointed to by <b>pElems</b>.


### -field pElems

A pointer to an array of values, each of which specifies a CLSID of a particular property page. This array is allocated by the callee using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and is freed by the caller using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ispecifypropertypages-getpages">ISpecifyPropertyPages::GetPages</a>
 

 

