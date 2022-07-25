---
UID: NE:callobj.CALLFRAME_FREE
title: CALLFRAME_FREE (callobj.h)
description: Determines the parameter type to be freed.
helpviewer_keywords: ["CALLFRAME_FREE","CALLFRAME_FREE enumeration [COM]","CALLFRAME_FREE_ALL","CALLFRAME_FREE_IN","CALLFRAME_FREE_INOUT","CALLFRAME_FREE_NONE","CALLFRAME_FREE_OUT","CALLFRAME_FREE_TOP_INOUT","CALLFRAME_FREE_TOP_OUT","_com_CALLFRAME_FREE","callobj/CALLFRAME_FREE","callobj/CALLFRAME_FREE_ALL","callobj/CALLFRAME_FREE_IN","callobj/CALLFRAME_FREE_INOUT","callobj/CALLFRAME_FREE_NONE","callobj/CALLFRAME_FREE_OUT","callobj/CALLFRAME_FREE_TOP_INOUT","callobj/CALLFRAME_FREE_TOP_OUT","com.callframe_free"]
old-location: com\callframe_free.htm
tech.root: com
ms.assetid: 6a048133-7a89-4b55-afd3-5eb722d41914
ms.date: 12/05/2018
ms.keywords: CALLFRAME_FREE, CALLFRAME_FREE enumeration [COM], CALLFRAME_FREE_ALL, CALLFRAME_FREE_IN, CALLFRAME_FREE_INOUT, CALLFRAME_FREE_NONE, CALLFRAME_FREE_OUT, CALLFRAME_FREE_TOP_INOUT, CALLFRAME_FREE_TOP_OUT, _com_CALLFRAME_FREE, callobj/CALLFRAME_FREE, callobj/CALLFRAME_FREE_ALL, callobj/CALLFRAME_FREE_IN, callobj/CALLFRAME_FREE_INOUT, callobj/CALLFRAME_FREE_NONE, callobj/CALLFRAME_FREE_OUT, callobj/CALLFRAME_FREE_TOP_INOUT, callobj/CALLFRAME_FREE_TOP_OUT, com.callframe_free
req.header: callobj.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLFRAME_FREE
 - callobj/CALLFRAME_FREE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CallObj.h
api_name:
 - CALLFRAME_FREE
---

# CALLFRAME_FREE enumeration


## -description

Determines the parameter type to be freed.

## -enum-fields

### -field CALLFRAME_FREE_NONE:0

No values are freed.

### -field CALLFRAME_FREE_IN:1

The [in] parameters are freed. This includes both top-level pointers and the data they reference.

### -field CALLFRAME_FREE_INOUT:2

The data referenced by [in, out] parameters are freed. However, the top-level pointers, which are the actual parameter values, are not freed.

On the server side, this is typically used post-call, as in CALLFRAME_FREE_IN. On the client side, this is typically used when the server was not actually invoked (and so unmarshaling of return values was not attempted) or when unmarshaling of the return values failed.

### -field CALLFRAME_FREE_OUT:4

The data referenced by [out] parameters are freed. However, the top-level pointers, which are the actual parameter values, are not freed.

On the server side, this is typically used post-call, as in CALLFRAME_FREE_IN. On the client side, this is typically only used when unmarshaling of return values failed.

### -field CALLFRAME_FREE_TOP_INOUT:8

The [in, out] parameters are freed. This includes both top-level pointers and the data they reference.

### -field CALLFRAME_FREE_TOP_OUT:16

The [out] parameters are freed. This includes both top-level pointers and the data they reference.

### -field CALLFRAME_FREE_ALL:31

All [in], [out], and [in, out] parameters are freed. This includes both top-level pointers and the data they reference.

## -see-also

<a href="/windows/desktop/api/callobj/nf-callobj-icallframe-free">ICallFrame::Free</a>



<a href="/windows/desktop/api/callobj/nf-callobj-icallframe-freeparam">ICallFrame::FreeParam</a>
