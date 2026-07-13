---
UID: NE:callobj.__MIDL_ICallFrame_0003
title: CALLFRAME_COPY (callobj.h)
description: Determines whether the copied call frame data can be shared with data in the parent frame by determining its lifetime dependency on the parent frame.
helpviewer_keywords: ["CALLFRAME_COPY","CALLFRAME_COPY enumeration [COM]","CALLFRAME_COPY_INDEPENDENT","CALLFRAME_COPY_NESTED","_com_CALLFRAME_COPY","callobj/CALLFRAME_COPY","callobj/CALLFRAME_COPY_INDEPENDENT","callobj/CALLFRAME_COPY_NESTED","com.callframe_copy"]
old-location: com\callframe_copy.htm
tech.root: com
ms.assetid: 06c926ab-8e82-4291-b1ea-f4bfcd734b16
ms.date: 12/05/2018
ms.keywords: CALLFRAME_COPY, CALLFRAME_COPY enumeration [COM], CALLFRAME_COPY_INDEPENDENT, CALLFRAME_COPY_NESTED, _com_CALLFRAME_COPY, callobj/CALLFRAME_COPY, callobj/CALLFRAME_COPY_INDEPENDENT, callobj/CALLFRAME_COPY_NESTED, com.callframe_copy
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
req.typenames: CALLFRAME_COPY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_ICallFrame_0003
 - callobj/__MIDL_ICallFrame_0003
 - CALLFRAME_COPY
 - callobj/CALLFRAME_COPY
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
 - CALLFRAME_COPY
---

# CALLFRAME_COPY enumeration


## -description

Determines whether the copied call frame data can be shared with data in the parent frame by determining its lifetime dependency on the parent frame.

## -enum-fields

### -field CALLFRAME_COPY_NESTED:1

The client will be responsible for using the copied call frame in a manner that its lifetime is nested in the lifetime of its parent frame making the data sharable. When this flag is used, very significant optimizations can be made and memory allocations avoided by cleverly sharing actual parameter data.

Only the interface pointers transitively reachable in the source frames are guaranteed to be deep copied and thus in the copy be stored in memory separate from that in which they are stored in the source frames; other data types may actually in the copied frame share memory with the source if the copy operation is intelligent enough to do so.

### -field CALLFRAME_COPY_INDEPENDENT:2

The copied call frame will have a lifetime independent from its parent.

## -remarks

A consequence is that whichever of these <b>CALLFRAME_COPY</b> flags are passed to <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-copy">ICallFrame::Copy</a>, the interface pointers can be modified without consequence of disturbing the interface pointers residing in the parent frame.

## -see-also

<a href="/windows/desktop/api/callobj/nf-callobj-icallframe-copy">ICallFrame::Copy</a>
