---
UID: NE:mfidl.MFSampleAllocatorUsage
title: MFSampleAllocatorUsage
ms.date: 11/4/2019
targetos: Windows
description: 
tech.root: mf
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfidl.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSampleAllocatorUsage
f1_keywords:
 - MFSampleAllocatorUsage
 - mfidl/MFSampleAllocatorUsage
dev_langs:
 - c++
---

## -description

Specifies the allocator usage of components that implement the [IMFSampleAllocatorControl](nn-mfidl-imfsampleallocatorcontrol.md) interface.

## -enum-fields

### -field MFSampleAllocatorUsage_UsesProvidedAllocator:0

The output stream will use the camera pipeline's sample allocator to allocate new media samples. If the output stream is producing samples in CPU memory, it is recommended that it use this mode to ensure consistent performance when used in a cross-container scenario.

### -field MFSampleAllocatorUsage_UsesCustomAllocator

The output stream will be use a custom allocator for its output samples.  It will not use the sample allocator provided by the camera pipeline.

### -field MFSampleAllocatorUsage_DoesNotAllocate

The output stream will not allocate new samples for its output samples.  It will not be provided a sample allocator by the camera pipeline.

## -remarks

Components should pass a value from the enumeration back from an implementation of [IMFSampleAllocatorControl::GetAllocatorUsage](nf-mfidl-imfsampleallocatorcontrol-getallocatorusage.md) to let the system know if they will use the system-provided allocator.

## -see-also

