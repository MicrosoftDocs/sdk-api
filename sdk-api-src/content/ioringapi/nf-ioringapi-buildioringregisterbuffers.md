---
UID: NF:ioringapi.BuildIoRingRegisterBuffers
tech.root: fs
title: BuildIoRingRegisterBuffers
ms.date: 07/16/2021
targetos: Windows
description: Registers an array of buffers with the system for future I/O ring operations.
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
 - BuildIoRingRegisterBuffers
f1_keywords:
 - BuildIoRingRegisterBuffers
 - ioringapi/BuildIoRingRegisterBuffers
dev_langs:
 - c++
---

## -description

Registers an array of buffers with the system for future I/O ring operations.

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring for which buffers are registered.

### -param count

A UINT32 specifying the number of buffers provided in the *buffers* parameter.

### -param buffers

An array of [IORING_BUFFER_INFO](../ntioring_x/ns-ntioring_x-ioring_buffer_info.md) structures representing the buffers to be registered.

### -param userData

A UINT_PTR value identifying the registration operation. Specify this value when cancelling the operation with a call to [BuildIoRingCancelRequest](nf-ioringapi-buildioringcancelrequest.md). If an app implements cancellation behavior for the operation, the *userData* value must be unique. Otherwise, the value is treated as opaque by the system and can be anything, including 0.

## -returns

Returns an HRESULT including, but not limited to the following:

| Value | Description |
|-------|-------------|
| S_OK  | Success |
| IORING_E_SUBMISSION_QUEUE_FULL | The submission queue is full, and no additional entries are available to build. The application must submit the existing entries and wait for some of them to complete before adding more operations to the queue. |
| IORING_E_UNKNOWN_REQUIRED_FLAG | The application provided a required flag that is not known to the implementation. Library code should check the *IoRingVersion* field of the [IORING_INFO](ns-ioringapi-ioring_info.md) obtained from a call to [GetIoRingInfo](nf-ioringapi-getioringinfo.md) to determine the API version of an I/O ring which determines the operations and flags that are supported. Applications should know the version they used to create the I/O ring and therefore should not provide unsupported flags at runtime. |

## -remarks

 This function allows the kernel implementation to perform the validation and internal mapping just once avoiding the overhead on each I/O operation. Subsequent entries in the submission queue may refer to the buffers registered with this function using an integer index into the array.  If a previous registration exists, this replaces the previous registration completely. Any entries in the array with an *Address* of NULL and a *Length* of 0 are sparse entries, and not used. This allows you to release one or more of the previously registered buffers.


## -see-also

