---
UID: NS:ioringapi.IORING_BUFFER_REF
tech.root: fs
title: IORING_BUFFER_REF
ms.date: 08/03/2022
targetos: Windows
description: IORING_BUFFER_REF represents a reference to a buffer used in an I/O ring operation.
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
req.typenames: IORING_BUFFER_REF
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ioringapi.h
api_name:
 - IORING_BUFFER_REF
f1_keywords:
 - IORING_BUFFER_REF
 - ioringapi/IORING_BUFFER_REF
dev_langs:
 - c++
---

## -description

Represents a reference to a buffer used in an I/O ring operation.

## -struct-fields

### -field Kind

A value from the [IORING_REF_KIND](ne-ioringapi-ioring_ref_kind.md) enumeration specifying the kind of buffer represented by the structure.

### -field BufferUnion

### -field BufferUnion.Address

A void pointer specifying the address of a buffer if the *Kind* value is IORING_REF_RAW.

### -field BufferUnion.IndexAndOffset

The index and offset of the registered buffer if the *Kind* value is IORING_REF_REGISTERED.

### -field Buffer

## -remarks

## -see-also

