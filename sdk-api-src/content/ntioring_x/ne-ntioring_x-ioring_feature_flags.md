---
UID: NE:ntioring_x.IORING_FEATURE_FLAGS
tech.root: fs
title: IORING_FEATURE_FLAGS
ms.date: 07/16/2021
targetos: Windows
description: Represents feature support for the an I/O ring API version.
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
 - IORING_FEATURE_FLAGS
f1_keywords:
 - IORING_FEATURE_FLAGS
 - ntioring_x/IORING_FEATURE_FLAGS
dev_langs:
 - c++
---

## -description

Represents feature support for the an I/O ring API version.

## -enum-fields

### -field IORING_FEATURE_FLAGS_NONE

None.

### -field IORING_FEATURE_UM_EMULATION

I/O ring support is emulated in User Mode. When this flag is set there is no underlying kernel support for I/O ring. However, a user mode emulation layer is available to provide application compatibility, without the benefit of kernel support.  This provides application compatibility at the expense of performance, allowing apps to make a choice at run-time. As of the current release, Microsoft does not provide an emulated I/O ring implementation. This value is provided to support potential emulated future emulated implementations.  

### -field IORING_FEATURE_SET_COMPLETION_EVENT

Registration of a completion queue event is supported. For more information, see [SetIoRingCompletionEvent](../ioringapi/nf-ioringapi-setioringcompletionevent.md).

## -remarks

## -see-also

