---
UID: NE:ioringapi.IORING_CREATE_ADVISORY_FLAGS
tech.root: fs
title: IORING_CREATE_ADVISORY_FLAGS
ms.date: 07/16/2021
targetos: Windows
description: Specifies advisory flags for creating an I/O ring with a call to CreateIoRing.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: ioringapi.h
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
 - ioringapi.h
api_name:
 - IORING_CREATE_ADVISORY_FLAGS
f1_keywords:
 - IORING_CREATE_ADVISORY_FLAGS
 - ioringapi/IORING_CREATE_ADVISORY_FLAGS
dev_langs:
 - c++
---

## -description

Specifies advisory flags for creating an I/O ring with a call to [CreateIoRing](nf-ioringapi-createioring.md).

## -enum-fields

### -field IORING_CREATE_ADVISORY_FLAGS_NONE

None.

## -remarks

Use the [IORING_CREATE_FLAGS](ns-ioringapi-ioring_create_flags.md) structure to pass flags into **CreateIoRing**. Any unknown or unsupported advisory flags provided to an API are ignored.

## -see-also

