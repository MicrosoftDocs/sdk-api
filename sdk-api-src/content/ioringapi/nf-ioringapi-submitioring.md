---
UID: NF:ioringapi.SubmitIoRing
tech.root: fs
title: SubmitIoRing
ms.date: 07/16/2021
targetos: Windows
description: Submits all constructed but not yet submitted entries to the kernel’s queue and optionally waits for a set of operations to complete.
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
 - SubmitIoRing
f1_keywords:
 - SubmitIoRing
 - ioringapi/SubmitIoRing
dev_langs:
 - c++
---

## -description

Submits all constructed but not yet submitted entries to the kernel’s queue and optionally waits for a set of operations to complete.

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring for which entries will be submitted.

### -param waitOperations

The number of completion queue entries to wait for. Specifying 0 indicates that the call should not wait. This value must be less than the sum of the number of entries in the submission queue and the number of operations currently in progress.

### -param milliseconds

The number of milliseconds to wait for the operations to complete. Specify **INFINITE** to wait indefinitely. This value is ignored if 0 is specified for *waitOperations*.

### -param submittedEntries

Optional. Receives a pointer to an array of **UINT_32** values representing the number of entries submitted.

## -returns

Returns an HRESULT including, but not limited to, one of the following:

| Value | Description |
|-------|-------------|
| S_OK  | All entries in the queue were submitted without error.         |
| IORING_E_WAIT_TIMEOUT | All operations were submitted without error and the subsequent wait timed out. |
| Any other error value | Failure to process the submission queue in its entirety. |


## -remarks

If this function returns an error other than IORING_E_WAIT_TIMEOUT, then all entries remain in the submission queue. Any errors processing a single submission queue entry results in a synchronous completion of that entry posted to the completion queue with an error status code for that operation. 

## -see-also

