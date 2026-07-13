---
UID: NF:ioringapi.CreateIoRing
tech.root: fs
title: CreateIoRing
ms.date: 07/16/2021
targetos: Windows
description: Creates a new instance of an I/O ring submission/completion queue pair and returns a handle for referencing the I/O ring.
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
req.lib: kernel32.Lib
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
 - CreateIoRing
f1_keywords:
 - CreateIoRing
 - ioringapi/CreateIoRing
dev_langs:
 - c++
---

## -description

Creates a new instance of an I/O ring submission/completion queue pair and returns a handle for referencing the IORING.

## -parameters

### -param ioringVersion

A UNIT32 representing the version of the I/O ring API the ring is created for. This value must be less than or equal to the value retrieved from a call to [QueryIoRingCapabilities](nf-ioringapi-queryioringcapabilities.md)

### -param flags

A value from the [IORING_CREATE_FLAGS](ns-ioringapi-ioring_create_flags.md) enumeration specifying creation flags.

### -param submissionQueueSize

The requested minimum submission queue size. The system may round up the size as needed to ensure the actual size is a power of 2. You can get the actual allocated queue size by calling [GetIoRingInfo](nf-ioringapi-getioringinfo.md). You can get the maximum submission queue size on the current system by calling [QueryIoRingCapabilities](nf-ioringapi-queryioringcapabilities.md).

### -param completionQueueSize

The requested minimum size of the completion queue. The system will round this size up to a power of two that is no less than two times the actual submission queue size to allow for submissions while some operations are still in progress. You can get the actual allocated queue size by calling [GetIoRingInfo](nf-ioringapi-getioringinfo.md).

### -param h

Receives the resulting **HIORING**  handle, if creation was successful. The returned **HIORING** ring must be closed by calling [CloseIoRing](nf-ioringapi-closeioring.md), not [CloseHandle](../handleapi/nf-handleapi-closehandle.md), to release the underlying resources for the IORING.

## -returns

An HRESULT, including but not limited to the following:

| Value | Description |
|-------|-------------|
| S_OK | Success. |
| IORING_E_UNKNOWN_VERSION | The version specified in *ioringVersion* is unknown. |

## -remarks

## -see-also

