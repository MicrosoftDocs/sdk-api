---
UID: NF:ioringapi.QueryIoRingCapabilities
tech.root: fs
title: QueryIoRingCapabilities
ms.date: 07/16/2021
targetos: Windows
description: Queries the OS for the supported capabilities for IORINGs.
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
req.lib: kernel32.Lib
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
 - api-ms-win-core-ioring-l1-1-2.dll
 - api-ms-win-core-ioring-l1-1-1.dll
 - api-ms-win-core-ioring-l1-1-0.dll
 - ioringapi.h
api_name:
 - QueryIoRingCapabilities
f1_keywords:
 - QueryIoRingCapabilities
 - ioringapi/QueryIoRingCapabilities
dev_langs:
 - c++
---

## -description

Queries the OS for the supported capabilities for I/O rings.

## -parameters

### -param capabilities

Receives a pointer to an [IORING_CAPABILITIES](ns-ioringapi-ioring_capabilities.md) representing the I/O ring API capabilities. 

## -returns

S_OK on success.

## -remarks

The results of this call are internally cached per-process, so this is efficient to call multiple times as only the first will transition to the kernel to retrieve the data.Note that the results are not guaranteed to contain the same values between runs of the same process or even between processes on the same system.  So applications should not store this information beyond the lifetime of the process and should not assume that other processes have the same support.

## -see-also

