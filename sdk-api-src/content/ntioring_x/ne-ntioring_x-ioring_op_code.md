---
UID: NE:ntioring_x.IORING_OP_CODE
tech.root: fs
title: IORING_OP_CODE
ms.date: 07/16/2021
targetos: Windows
description: Specifies the type of an I/O ring operation.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: ntioring_x.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ntioring_x.h
api_name:
 - IORING_OP_CODE
f1_keywords:
 - IORING_OP_CODE
 - ntioring_x/IORING_OP_CODE
dev_langs:
 - c++
---

## -description

Specifies the type of an I/O ring operation.

## -enum-fields

### -field IORING_OP_NOP

No operation. This value is provided to enable testing queue management and overhead performance./

### -field IORING_OP_READ

Read from a file to a buffer.

### -field IORING_OP_REGISTER_FILES

Register an array of file handles with the I/O ring.

If any existing registration exists, it is completely replaced by the registration for this opcode. Any entries in the array with INVALID_HANDLE_VALUE are sparse entries and are not used, which can be used to release one or more of the previously registered files. 

Unregistration of all current files is accomplished by providing a zero length array. The input array must remain valid until the operation completes. The change impacts all entries in the queue after this completes. I.e. This implicitly has "link" semantics in that any subsequent entry will not start until after this is completed.

### -field IORING_OP_REGISTER_BUFFERS

Register an array of [IORING_BUFFER_INFO](ns-ntioring_x-ioring_buffer_info.md) with the IORING.

If any existing registration exists, it is completely replaced by the registration for this opcode. Any entries in the array with INVALID_HANDLE_VALUE are sparse entries and are not used, which can be used to release one or more of the previously registered files. 

Unregistration of all current files is accomplished by providing a zero length array. The input array must remain valid until the operation completes. The change impacts all entries in the queue after this completes. I.e. This implicitly has "link" semantics in that any subsequent entry will not start until after this is completed.

### -field IORING_OP_CANCEL

Request cancellation of a previously submitted operation. The *UserData* passed in when the operation was initiated is used to identify the operation to be cancelled. The cancellation operation completes after the canceled operation completes unless there is an error attempting the cancellation. For example, if no operation is found with the specified *UserData*.


## -remarks

## -see-also

