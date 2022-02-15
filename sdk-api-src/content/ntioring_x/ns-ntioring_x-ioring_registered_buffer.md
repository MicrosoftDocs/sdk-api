---
UID: NS:ntioring_x.IORING_REGISTERED_BUFFER
tech.root: fs
title: IORING_REGISTERED_BUFFER
ms.date: 07/16/2021
targetos: Windows
description: Represents a buffer that has been registered with an I/O ring with a call to BuildIoRingRegisterBuffers.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ntioring_x.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000 
req.target-type: 
req.typenames: IORING_REGISTERED_BUFFER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ntioring_x.h
api_name:
 - IORING_REGISTERED_BUFFER
f1_keywords:
 - IORING_REGISTERED_BUFFER
 - ntioring_x/IORING_REGISTERED_BUFFER
dev_langs:
 - c++
---

## -description

Represents a buffer that has been registered with an I/O ring with a call to [BuildIoRingRegisterBuffers](../ioringapi/nf-ioringapi-buildioringregisterbuffers.md).

## -struct-fields

### -field BufferIndex

A **UINT32** specifying the index of the registered buffer.

### -field Offset

A **UINT32** specifying the offset into the registered buffer.

## -remarks

By using both a buffer index within the submission queue and an offset within the buffer, you can use large buffers and schedule multiple I/O ring operations within the same buffer to be performed asynchronously.

## -see-also

