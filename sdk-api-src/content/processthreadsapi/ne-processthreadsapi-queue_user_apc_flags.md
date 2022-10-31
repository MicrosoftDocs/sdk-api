---
UID: NE:processthreadsapi._QUEUE_USER_APC_FLAGS
title: QUEUE_USER_APC_FLAGS (processthreadsapi.h)
description: The QUEUE_USER_APC_FLAGS enumeration (processthreadsapi.h) specifies the modifier flags for user-mode asynchronous procedure call (APC) objects.
tech.root: processthreadsapi
ms.date: 12/05/2018
helpviewer_keywords: ["QUEUE_USER_APC_FLAGS"]
ms.keywords: 'QUEUE_USER_APC_FLAGS'
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
req.typenames: QUEUE_USER_APC_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QUEUE_USER_APC_FLAGS
 - processthreadsapi/_QUEUE_USER_APC_FLAGS
 - QUEUE_USER_APC_FLAGS
 - processthreadsapi/QUEUE_USER_APC_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - QUEUE_USER_APC_FLAGS
---


# QUEUE_USER_APC_FLAGS enumeration

## -description

Specifies the modifier flags for user-mode asynchronous procedure call (APC) objects.

## -enum-fields

### -field QUEUE_USER_APC_FLAGS_NONE

No flags are passed. Behavior is identical to [QueueUserAPC function](nf-processthreadsapi-queueuserapc.md).

### -field QUEUE_USER_APC_FLAGS_SPECIAL_USER_APC

Queue a special user-mode APC instead of a regular user-mode APC.

### -field QUEUE_USER_APC_CALLBACK_DATA_CONTEXT

Receive the processor context that was interrupted when the thread was directed to call the APC function.

## -remarks

The *Parameter* argument of the [PAPCFUNC callback function](../winnt/nc-winnt-papcfunc.md) is modified to point to an APC_CALLBACK_DATA structure (see below), which contains the original *Parameter* argument, a pointer to the interrupted processor context, and reserved fields.

```cpp
typedef struct _APC_CALLBACK_DATA {
    ULONG_PTR Parameter;
    PCONTEXT ContextRecord;
    ULONG_PTR Reserved0;
    ULONG_PTR Reserved1;
} APC_CALLBACK_DATA, *PAPC_CALLBACK_DATA;
```

## -see-also

[QueueUserAPC2](nf-processthreadsapi-queueuserapc2.md)
