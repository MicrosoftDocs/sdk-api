---
UID: NF:mfidl.IMFVideoSampleAllocatorCallback.GetFreeSampleCount
title: IMFVideoSampleAllocatorCallback::GetFreeSampleCount (mfidl.h)
description: Gets the number of video samples that are currently available for use.
helpviewer_keywords: ["GetFreeSampleCount","GetFreeSampleCount method [Media Foundation]","GetFreeSampleCount method [Media Foundation]","IMFVideoSampleAllocatorCallback interface","IMFVideoSampleAllocatorCallback interface [Media Foundation]","GetFreeSampleCount method","IMFVideoSampleAllocatorCallback.GetFreeSampleCount","IMFVideoSampleAllocatorCallback::GetFreeSampleCount","mf.imfvideosampleallocatorcallback_getfreesamplecount","mfidl/IMFVideoSampleAllocatorCallback::GetFreeSampleCount"]
old-location: mf\imfvideosampleallocatorcallback_getfreesamplecount.htm
tech.root: mf
ms.assetid: 0025067b-1c8f-4f1a-91f2-edf6a274523b
ms.date: 12/05/2018
ms.keywords: GetFreeSampleCount, GetFreeSampleCount method [Media Foundation], GetFreeSampleCount method [Media Foundation],IMFVideoSampleAllocatorCallback interface, IMFVideoSampleAllocatorCallback interface [Media Foundation],GetFreeSampleCount method, IMFVideoSampleAllocatorCallback.GetFreeSampleCount, IMFVideoSampleAllocatorCallback::GetFreeSampleCount, mf.imfvideosampleallocatorcallback_getfreesamplecount, mfidl/IMFVideoSampleAllocatorCallback::GetFreeSampleCount
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoSampleAllocatorCallback::GetFreeSampleCount
 - mfidl/IMFVideoSampleAllocatorCallback::GetFreeSampleCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoSampleAllocatorCallback.GetFreeSampleCount
---

# IMFVideoSampleAllocatorCallback::GetFreeSampleCount


## -description

Gets the number of video samples that are currently available for use.

## -parameters

### -param plSamples [out]

Receives the number of available samples.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get a video sample from the allocator, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-allocatesample">IMFVideoSampleAllocator::AllocateSample</a> method. The <b>AllocateSample</b> method removes a sample from the sample pool and returns it to the caller. When a sample is released, it returns to the pool. The <b>GetFreeSampleCount</b> method returns the count of samples that remain in the sample pool.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback">IMFVideoSampleAllocatorCallback</a>