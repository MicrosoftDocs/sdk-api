---
UID: NF:ioringapi.GetIoRingInfo
tech.root: fs
title: GetIoRingInfo
ms.date: 07/16/2021
targetos: Windows
description: Gets information about the API version and queue sizes of an I/O ring.
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
 - 
api_location:
 - ioringapi.h
api_name:
 - GetIoRingInfo
f1_keywords:
 - GetIoRingInfo
 - ioringapi/GetIoRingInfo
dev_langs:
 - c++
---

## -description

Gets information about the API version and queue sizes of an I/O ring.

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring for which information is being queried.

### -param info

Receives a pointer to an [IORING_INFO](ns-ioringapi-ioring_info.md) structure specifying API version and queue sizes for the specified I/O ring.

## -returns

S_OK on success.

## -remarks

## -see-also

