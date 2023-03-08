---
UID: NF:mfidl.IMFSampleAllocatorControl.SetDefaultAllocator
title: IMFSampleAllocatorControl::SetDefaultAllocator
ms.date: 11/4/2019
targetos: Windows
description: Sets the default sample allocator to use for the specified output stream.
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
 - IMFSampleAllocatorControl::SetDefaultAllocator
f1_keywords:
 - IMFSampleAllocatorControl::SetDefaultAllocator
 - mfidl/IMFSampleAllocatorControl::SetDefaultAllocator
dev_langs:
 - c++
---

## -description

Sets the default sample allocator to use for the specified output stream.

## -parameters

### -param dwOutputStreamID

The ID of the output stream that the *pAllocator* parameter applies to.

### -param pAllocator

Receives a pointer to a sample allocator to use for the specified output stream. The
allocator supports one of the MF allocator interfaces, such as [IMFVideoCaptureSampleAllocator](nn-mfidl-imfvideocapturesampleallocator.md) or [IMFVideoSampleAllocatorEx](nn-mfidl-imfvideosampleallocatorex.md).

## -returns

The method returns an **HRESULT**.

## -remarks

The system calls this method to provide components with a sample allocator that allows the component to allocate samples using memory that is accessible from within a container.

Components that use the provided allocator should return [MFSampleAllocatorUsage_UsesProvidedAllocator](ne-mfidl-mfsampleallocatorusage.md) from calls to [IMFSampleAllocatorControl::GetAllocatorUsage](nf-mfidl-imfsampleallocatorcontrol-setdefaultallocator.md).

## -see-also

