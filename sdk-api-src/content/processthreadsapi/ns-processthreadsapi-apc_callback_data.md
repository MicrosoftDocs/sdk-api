---
UID: NS:processthreadsapi._APC_CALLBACK_DATA
tech.root: backup
title: APC_CALLBACK_DATA
description: The APC_CALLBACK_DATA structure (processthreadsapi.h) specifies the data for a user-mode asynchronous procedure call (APC) object.
ms.date: 08/05/2022
targetos: Windows
description: 
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: processthreadsapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: APC_CALLBACK_DATA, *PAPC_CALLBACK_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - _APC_CALLBACK_DATA
 - PAPC_CALLBACK_DATA
 - APC_CALLBACK_DATA
f1_keywords:
 - _APC_CALLBACK_DATA
 - processthreadsapi/_APC_CALLBACK_DATA
 - PAPC_CALLBACK_DATA
 - processthreadsapi/PAPC_CALLBACK_DATA
 - APC_CALLBACK_DATA
 - processthreadsapi/APC_CALLBACK_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _APC_CALLBACK_DATA
---

# APC_CALLBACK_DATA structure

## -description

Specifies the data for a user-mode asynchronous procedure call (APC) object.

## -struct-fields

### -field Parameter

The data passed to the function using the dwData parameter of the [QueueUserAPC](nf-processthreadsapi-queueuserapc.md) function.

### -field ContextRecord

The processor context that was interrupted when the thread was directed to call the APC function.

### -field Reserved0

Reserved for future use; must be zero.

### -field Reserved1

Reserved for future use; must be zero.

## -remarks

## -see-also
