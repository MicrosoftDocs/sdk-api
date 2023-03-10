---
UID: NS:processthreadsapi._THREAD_POWER_THROTTLING_STATE
title: THREAD_POWER_THROTTLING_STATE (processthreadsapi.h)
description: Specifies the throttling policies and how to apply them to a target thread when that thread is subject to power management.
helpviewer_keywords: ["PTHREAD_POWER_THROTTLING_STATE","PTHREAD_POWER_THROTTLING_STATE structure pointer","THREAD_POWER_THROTTLING_CURRENT_VERSION","THREAD_POWER_THROTTLING_EXECUTION_SPEED","THREAD_POWER_THROTTLING_STATE","THREAD_POWER_THROTTLING_STATE structure","base.thread_power_throttling_state","processthreadsapi/PTHREAD_POWER_THROTTLING_STATE","processthreadsapi/THREAD_POWER_THROTTLING_STATE"]
old-location: base\thread_power_throttling_state.htm
tech.root: processthreadsapi
ms.assetid: 2E4D3A93-F4EE-4293-BE28-239B48E869B4
ms.date: 12/05/2018
ms.keywords: PTHREAD_POWER_THROTTLING_STATE, PTHREAD_POWER_THROTTLING_STATE structure pointer, THREAD_POWER_THROTTLING_CURRENT_VERSION, THREAD_POWER_THROTTLING_EXECUTION_SPEED, THREAD_POWER_THROTTLING_STATE, THREAD_POWER_THROTTLING_STATE structure, base.thread_power_throttling_state, processthreadsapi/PTHREAD_POWER_THROTTLING_STATE, processthreadsapi/THREAD_POWER_THROTTLING_STATE
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: THREAD_POWER_THROTTLING_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _THREAD_POWER_THROTTLING_STATE
 - processthreadsapi/_THREAD_POWER_THROTTLING_STATE
 - THREAD_POWER_THROTTLING_STATE
 - processthreadsapi/THREAD_POWER_THROTTLING_STATE
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
 - THREAD_POWER_THROTTLING_STATE
---

# THREAD_POWER_THROTTLING_STATE structure


## -description

Specifies the throttling policies and how to apply them to a target thread when that thread is subject to power management. This structure is used by the [SetThreadInformation function](./nf-processthreadsapi-setthreadinformation.md).

## -struct-fields

### -field Version

The version of the <b>THREAD_POWER_THROTTLING_STATE</b> structure.

| Value | Meaning |
| ---   | ---     |
| THREAD_POWER_THROTTLING_CURRENT_VERSION | The current version. |

### -field ControlMask

This field enables the caller to take control of the power throttling mechanism.

| Value | Meaning |
| ---   | ---     |
| THREAD_POWER_THROTTLING_EXECUTION_SPEED | Manages the execution speed of the thread. |

### -field StateMask

Manages the power throttling mechanism on/off state.

| Value | Meaning |
| ---   | ---     |
| THREAD_POWER_THROTTLING_EXECUTION_SPEED | Manages the execution speed of the thread. |