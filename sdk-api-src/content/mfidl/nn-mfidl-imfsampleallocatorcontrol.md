---
UID: NN:mfidl.IMFSampleAllocatorControl
title: IMFSampleAllocatorControl
ms.date: 1/23/2020
targetos: Windows
description: Implemented by video capture sources and transforms. Allows the system to provide components with a sample allocator to allocate samples using memory that is accessible from within a container.
tech.root: mf
req.assembly: mfuuid.dl
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSampleAllocatorControl
f1_keywords:
 - IMFSampleAllocatorControl
 - mfidl/IMFSampleAllocatorControl
dev_langs:
 - c++
---

## -description

Implemented by video capture sources and transforms. Allows the system to provide components with a sample allocator to allocate samples using memory that is accessible from within a container.

## -remarks

Components that do not implement this interface, or do not use the allocator provided by the system, can still allocate samples, but when running from inside a container, the system will have to copy all samples into container memory, which is less efficient.

## -see-also

