---
UID: NS:ioringapi.IORING_INFO
tech.root: fs
title: IORING_INFO
ms.date: 07/16/2021
targetos: Windows
description: Represents the shape and version information for the specified I/O ring.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ioringapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: IORING_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ioringapi.h
api_name:
 - IORING_INFO
f1_keywords:
 - IORING_INFO
 - ioringapi/IORING_INFO
dev_langs:
 - c++
---

## -description

Represents the shape and version information for the specified I/O ring.

## -struct-fields

### -field IoRingVersion

A [IORING_VERSION](../ntioring_x/ne-ntioring_x-ioring_version.md) structure representing the API version of the associated I/O ring.

### -field Flags

A [IORING_CREATE_FLAGS](ns-ioringapi-ioring_create_flags.md) structure containing the creation flags with which the associated I/O ring.

### -field SubmissionQueueSize

The actual minimum submission queue size. The system may round up the value requested in the call to [CreateIoRing](nf-ioringapi-createioring.md) as needed to ensure the actual size is a power of 2. 

### -field CompletionQueueSize

The actual minimum size of the completion queue. The system will round up the value requested in the call to **CreateIoRing** to a power of two that is no less than two times the actual submission queue size to allow for submissions while some operations are still in progress.

## -remarks

## -see-also

