---
UID: NF:ioringapi.IoRingBufferRefFromIndexAndOffset
tech.root: fs
title: IoRingBufferRefFromIndexAndOffset
ms.date: 07/16/2021
targetos: Windows
description: Creates an instance of the IORING_BUFFER_REF structure with the provided buffer index and offset.
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
 - ioringapi.h
api_name:
 - IoRingBufferRefFromIndexAndOffset
f1_keywords:
 - IoRingBufferRefFromIndexAndOffset
 - ioringapi/IoRingBufferRefFromIndexAndOffset
dev_langs:
 - c++
---

## -description

Creates an instance of the [IORING_BUFFER_REF](ns-ioringapi-ioring_buffer_ref.md) structure from the provided buffer index and offset.

## -parameters

### -param i

The index within the submission queue of the referenced buffer.

### -param o

The offset within the buffer specified by *index*.

## -remarks

## -see-also

