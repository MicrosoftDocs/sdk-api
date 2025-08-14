---
UID: NF:ioringapi.BuildIoRingReadFile
tech.root: fs
title: BuildIoRingReadFile
ms.date: 07/16/2021
targetos: Windows
description: Performs an asynchronous read from a file using an I/O ring. 
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
 - BuildIoRingReadFile
f1_keywords:
 - BuildIoRingReadFile
 - ioringapi/BuildIoRingReadFile
dev_langs:
 - c++
---

## -description

Performs an asynchronous read from a file using an I/O ring. This operation is similar to calling [ReadFileEx](../fileapi/nf-fileapi-readfileex.md).

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring which will perform the read operation.

### -param fileRef

An [IORING_HANDLE_REF](ns-ioringapi-ioring_handle_ref.md) specifying the file to read.

### -param dataRef

An [IORING_BUFFER_REF](ns-ioringapi-ioring_buffer_ref.md) specifying the buffer into which the file is read. The provided buffer must have a size of at least *numberOfBytesToRead* bytes.

### -param numberOfBytesToRead

The number of bytes to read.

### -param fileOffset

The offset into the file to begin reading.

### -param userData

A UINT_PTR value identifying the file read operation. Specify this value when cancelling the operation with a call to [BuildIoRingCancelRequest](nf-ioringapi-buildioringcancelrequest.md). If an app implements cancellation behavior for the operation, the *userData* value must be unique. Otherwise, the value is treated as opaque by the system and can be anything, including 0.

### -param flags

A bitwise OR combination of values from the [IORING_SQE_FLAGS](ne-ioringapi-ioring_sqe_flags.md) enumeration specifying kernel behavior options for I/O ring submission queue entries.

## -returns

Returns an HRESULT including, but not limited to the following:

| Value | Description |
|-------|-------------|
| S_OK  | Success |
| IORING_E_SUBMISSION_QUEUE_FULL | The submission queue is full, and no additional entries are available to build. The application must submit the existing entries and wait for some of them to complete before adding more operations to the queue. |
| IORING_E_UNKNOWN_REQUIRED_FLAG | The application provided a required flag that is not known to the implementation. Library code should check the *IoRingVersion* field of the [IORING_INFO](ns-ioringapi-ioring_info.md) obtained from a call to [GetIoRingInfo](nf-ioringapi-getioringinfo.md) to determine the API version of an I/O ring which determines the operations and flags that are supported. Applications should know the version they used to create the I/O ring and therefore should not provide unsupported flags at runtime. |

## -remarks

Check I/O ring support for read file operations by calling [IsIoRingOpSupported](nf-ioringapi-isioringopsupported.md) and specifying [IORING_OP_READ](../ntioring_x/ne-ntioring_x-ioring_op_code.md) for the *op* parameter.

## -see-also

