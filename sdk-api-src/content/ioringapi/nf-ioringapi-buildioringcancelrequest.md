---
UID: NF:ioringapi.BuildIoRingCancelRequest
tech.root: fs
title: BuildIoRingCancelRequest
ms.date: 07/16/2021
targetos: Windows
description: Attempts to cancel a previously submitted I/O ring operation.
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
 - BuildIoRingCancelRequest
f1_keywords:
 - BuildIoRingCancelRequest
 - ioringapi/BuildIoRingCancelRequest
dev_langs:
 - c++
---

## -description

Attempts to cancel a previously submitted I/O ring operation.

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring for which a cancellation is requested.

### -param file

An [IORING_HANDLE_REF](ns-ioringapi-ioring_handle_ref.md) representing the file associated with the operation to cancel.

### -param opToCancel

A **UINT_PTR** specifying the operation to cancel. This value is the same value provided in the *userData* parameter when the operation was registered. To support cancellation, the *userData* value must be unique for each operation.

### -param userData

A UINT_PTR value identifying the cancellation operation. Specify this value when cancelling the operation with a call to [BuildIoRingCancelRequest](nf-ioringapi-buildioringcancelrequest.md). If an app implements cancellation behavior for the operation, the *userData* value must be unique. Otherwise, the value is treated as opaque by the system and can be anything, including 0.


## -returns


| Value | Description |
|-------|-------------|
| S_OK  | Success |
| IORING_E_SUBMISSION_QUEUE_FULL | The submission queue is full, and no additional entries are available to build. The application must submit the existing entries and wait for some of them to complete before adding more operations to the queue. |
| IORING_E_UNKNOWN_REQUIRED_FLAG | The application provided a required flag that is not known to the implementation. Library code should check the *IoRingVersion* field of the [IORING_INFO](ns-ioringapi-ioring_info.md) obtained from a call to [GetIoRingInfo](nf-ioringapi-getioringinfo.md) to determine the API version of an I/O ring which determines the operations and flags that are supported. Applications should know the version they used to create the I/O ring and therefore should not provide unsupported flags at runtime. |

## -remarks

Since I/O ring operations are performed asynchronously this function call is only a request for cancellation. The specified operation may complete before the cancellation is processed. The cancellation operation may complete after the operation it is canceling is completed. The completion of the cancel operation is not dependent on the actual completion of the I/O operations it cancels. Apps should look for the completion of the original operation in the completion queue by calling [PopIoRingCompletion](nf-ioringapi-popioringcompletion.md) to observe the final status of the operation. The operation may have completed successfully or with an error rather than being cancelled by the call to this function. 

## -see-also

