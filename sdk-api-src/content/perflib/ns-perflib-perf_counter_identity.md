---
UID: NS:perflib._PERF_COUNTER_IDENTITY
title: PERF_COUNTER_IDENTITY (perflib.h)
description: Defines the counter that is sent to a provider's callback when the consumer adds or removes a counter from the query.
helpviewer_keywords: ["*PPERF_COUNTER_IDENTITY","PERF_COUNTER_IDENTITY","PERF_COUNTER_IDENTITY structure [Perf]","PERF_COUNTER_IDENTITY","*PPERF_COUNTER_IDENTITY","PERF_COUNTER_IDENTITY","*PPERF_COUNTER_IDENTITY structure [Perf]","base.perf_counter_identity","perf.perf_counter_identity","perflib/PERF_COUNTER_IDENTITY"]
old-location: perf\perf_counter_identity.htm
tech.root: perf
ms.assetid: a18d2546-642b-4e83-be05-4b4aae1f2d2c
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTER_IDENTITY, PERF_COUNTER_IDENTITY, PERF_COUNTER_IDENTITY structure [Perf], PERF_COUNTER_IDENTITY,*PPERF_COUNTER_IDENTITY, PERF_COUNTER_IDENTITY,*PPERF_COUNTER_IDENTITY structure [Perf], base.perf_counter_identity, perf.perf_counter_identity, perflib/PERF_COUNTER_IDENTITY'
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PERF_COUNTER_IDENTITY, *PPERF_COUNTER_IDENTITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTER_IDENTITY
 - perflib/_PERF_COUNTER_IDENTITY
 - PPERF_COUNTER_IDENTITY
 - perflib/PPERF_COUNTER_IDENTITY
 - PERF_COUNTER_IDENTITY
 - perflib/PERF_COUNTER_IDENTITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_COUNTER_IDENTITY, *PPERF_COUNTER_IDENTITY
---

# PERF_COUNTER_IDENTITY structure


## -description

Defines the counter that is sent to a provider's callback when the consumer adds or removes a counter from the query.

## -struct-fields

### -field CounterSetGuid

GUID that uniquely identifies the counter set that this counter belongs to.

### -field BufferSize

Size, in bytes, of this structure and the computer name and instance name that are appended to this structure in memory.

### -field CounterId

Unique identifier of the counter in the counter set. 

This member is set to <b>PERF_WILDCARD_COUNTER</b> if the consumer wants to add or remove all counters in the counter set.

### -field InstanceId

Identifier of the counter set instance to which the counter belongs. 

Ignore this value if the instance name at <b>NameOffset</b> is PERF_WILDCARD_INSTANCE.

### -field MachineOffset

Offset to the null-terminated Unicode computer name that follows this structure in memory.

### -field NameOffset

Offset to the null-terminated Unicode instance name that follows this structure in memory.

### -field Reserved

Reserved.

## -see-also

<a href="/windows/desktop/api/perflib/nc-perflib-perflibrequest">ControlCallback</a>