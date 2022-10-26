---
UID: NE:processthreadsapi._QUEUE_USER_APC_FLAGS
tech.root: processthreadsapi
title: QUEUE_USER_APC_FLAGS (processthreadsapi.h)
description: The QUEUE_USER_APC_FLAGS enumeration (processthreadsapi.h) specifies the modifier flags for user-mode asynchronous procedure call (APC) objects.
ms.date: 08/05/2022
targetos: Windows
description: 
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: processthreadsapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - _QUEUE_USER_APC_FLAGS
 - QUEUE_USER_APC_FLAGS
f1_keywords:
 - _QUEUE_USER_APC_FLAGS
 - processthreadsapi/_QUEUE_USER_APC_FLAGS
 - QUEUE_USER_APC_FLAGS
 - processthreadsapi/QUEUE_USER_APC_FLAGS
helpviewer_keywords: ["QUEUE_USER_APC_FLAGS"]
dev_langs:
 - c++
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

The *Parameter* argument of the [PAPCFUNC callback function](../winnt/nc-winnt-papcfunc.md) is modified to point to an APC_CALLBACK_DATA structure (see below), which contains the original *Parameter* argument, a pointer to the interrupted processor context, and reserved fields.

```c++
typedef struct _APC_CALLBACK_DATA {
    ULONG_PTR Parameter;
    PCONTEXT ContextRecord;
    ULONG_PTR Reserved0;
    ULONG_PTR Reserved1;
} APC_CALLBACK_DATA, *PAPC_CALLBACK_DATA;
```

## -remarks

## -see-also

[QueueUserAPC2](nf-processthreadsapi-queueuserapc2.md)
