---
UID: NE:processthreadsapi._APC_CALLBACK_DATA
title: APC_CALLBACK_DATA (processthreadsapi.h)
description: The APC_CALLBACK_DATA structure (processthreadsapi.h) specifies the data for a user-mode asynchronous procedure call (APC) object.
tech.root: processthreadsapi
ms.date: 10/31/2022
helpviewer_keywords: ["APC_CALLBACK_DATA"]
ms.keywords: 'APC_CALLBACK_DATA'
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
req.typenames: APC_CALLBACK_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _APC_CALLBACK_DATA
 - processthreadsapi/_APC_CALLBACK_DATA
 - APC_CALLBACK_DATA
 - processthreadsapi/APC_CALLBACK_DATA
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
 - APC_CALLBACK_DATA
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
