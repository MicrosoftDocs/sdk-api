---
UID: NF:mfidl.IMFSampleAllocatorControl.GetAllocatorUsage
title: IMFSampleAllocatorControl::GetAllocatorUsage
ms.date: 11/4/2019
targetos: Windows
description: Retrieves the sample allocator usage for the specified output stream.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfuuid.dll
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSampleAllocatorControl::GetAllocatorUsage
f1_keywords:
 - IMFSampleAllocatorControl::GetAllocatorUsage
 - mfidl/IMFSampleAllocatorControl::GetAllocatorUsage
dev_langs:
 - c++
---

## -description

Retrieves the sample allocator usage for the specified output stream.

## -parameters

### -param dwOutputStreamID

The ID of the output stream whose sample allocator usage is requested.

### -param pdwInputStreamID

If the allocator usage is [MFSampleAllocatorUsage_DoesNotAllocate](ne-mfidl-mfsampleallocatorusage.md), then this output parameter is set to the ID of the input stream that the output samples are coming from. For all other allocator usage values, this parameter is ignored.

### -param peUsage

A member of the [MFSampleAllocatorUsage](ne-mfidl-mfsampleallocatorusage.md) enumeration specifying the sample allocator usage of the specified output stream.

## -returns

The method returns an **HRESULT**.

## -remarks

## -see-also

