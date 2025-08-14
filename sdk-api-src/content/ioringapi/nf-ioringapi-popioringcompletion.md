---
UID: NF:ioringapi.PopIoRingCompletion
tech.root: fs
title: PopIoRingCompletion
ms.date: 07/16/2021
targetos: Windows
description: Pops a single entry from the completion queue, if one is available. 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ioringapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-ioring-l1-1-2.dll
 - api-ms-win-core-ioring-l1-1-1.dll
 - api-ms-win-core-ioring-l1-1-0.dll
 - ioringapi.h
api_name:
 - PopIoRingCompletion
f1_keywords:
 - PopIoRingCompletion
 - ioringapi/PopIoRingCompletion
dev_langs:
 - c++
---

## -description

Pops a single entry from the completion queue, if one is available. 

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring from which an entry from the completion queue is popped.

### -param cqe

Pointer to an [IORING_CQE](ns-ioringapi-ioring_cqe.md) structure that will recieve the data for the completed queue entry.

## -returns

Returns an HRESULT including, but not limitted to the following:

| Value | Description |
|-------|-------------|
| S_OK  | The entry was popped from the queue and the **IORING_CQE** pointed to by *cqe* contains the values from the entry. |
| S_FALSE | The completion queue is empty, and the data pointed to by the *cqe* parameter is unmodified. |

## -remarks

## -see-also

