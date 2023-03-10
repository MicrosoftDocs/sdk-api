---
UID: NE:ioringapi.IORING_REF_KIND
tech.root: fs
title: IORING_REF_KIND
ms.date: 07/16/2021
targetos: Windows
description: Specifies the type of an IORING_HANDLE_REF structure.
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
 - IORING_REF_KIND
f1_keywords:
 - IORING_REF_KIND
 - ioringapi/IORING_REF_KIND
dev_langs:
 - c++
---

## -description

Specifies the type of an [IORING_HANDLE_REF](ns-ioringapi-ioring_handle_ref.md) structure.

## -enum-fields

### -field IORING_REF_RAW

The referenced buffer is raw.

### -field IORING_REF_REGISTERED

The referenced buffer has been registered with an I/O ring with a call to [BuildIoRingRegisterFileHandles](nf-ioringapi-buildioringregisterfilehandles.md)

## -remarks

## -see-also

