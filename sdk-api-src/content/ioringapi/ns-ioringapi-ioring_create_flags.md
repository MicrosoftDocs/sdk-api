---
UID: NS:ioringapi.IORING_CREATE_FLAGS
tech.root: fs
title: IORING_CREATE_FLAGS
ms.date: 07/16/2021
targetos: Windows
description: Specifies flags for creating an I/O ring with a call to CreateIoRing.
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
req.typenames: IORING_CREATE_FLAGS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ioringapi.h
api_name:
 - IORING_CREATE_FLAGS
f1_keywords:
 - IORING_CREATE_FLAGS
 - ioringapi/IORING_CREATE_FLAGS
dev_langs:
 - c++
---

## -description

Specifies flags for creating an I/O ring with a call to [CreateIoRing](nf-ioringapi-createioring.md).

## -struct-fields

### -field Required

A bitwise OR combination of flags from the [IORING_CREATE_REQUIRED_FLAGS](ne-ioringapi-ioring_create_required_flags.md) enumeration. If any unknown required flags are provided to an API, the API will fail the associated call.

### -field Advisory

A bitwise OR combination of flags from the [IORING_CREATE_ADVISORY_FLAGS](ne-ioringapi-ioring_create_advisory_flags.md) enumeration.Advisory flags. Any unknown or unsupported advisory flags provided to an API are ignored.

## -remarks

## -see-also

