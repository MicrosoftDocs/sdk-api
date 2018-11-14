---
UID: NF:mfidl.IMFVideoSampleAllocatorCallback.GetFreeSampleCount
title: IMFVideoSampleAllocatorCallback::GetFreeSampleCount
author: windows-sdk-content
description: Gets the number of video samples that are currently available for use.
old-location: mf\imfvideosampleallocatorcallback_getfreesamplecount.htm
tech.root: medfound
ms.assetid: 0025067b-1c8f-4f1a-91f2-edf6a274523b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetFreeSampleCount, GetFreeSampleCount method [Media Foundation], GetFreeSampleCount method [Media Foundation],IMFVideoSampleAllocatorCallback interface, IMFVideoSampleAllocatorCallback interface [Media Foundation],GetFreeSampleCount method, IMFVideoSampleAllocatorCallback.GetFreeSampleCount, IMFVideoSampleAllocatorCallback::GetFreeSampleCount, mf.imfvideosampleallocatorcallback_getfreesamplecount, mfidl/IMFVideoSampleAllocatorCallback::GetFreeSampleCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoSampleAllocatorCallback.GetFreeSampleCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFVideoSampleAllocatorCallback.GetFreeSampleCount
: 
---

# IMFVideoSampleAllocatorCallback::GetFreeSampleCount


## -description


Gets the number of video samples that are currently available for use.


## -parameters




### -param plSamples [out]

Receives the number of available samples.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get a video sample from the allocator, call the <a href="https://msdn.microsoft.com/e5347cef-edbd-4f6a-88c9-042e53515a32">IMFVideoSampleAllocator::AllocateSample</a> method. The <b>AllocateSample</b> method removes a sample from the sample pool and returns it to the caller. When a sample is released, it returns to the pool. The <b>GetFreeSampleCount</b> method returns the count of samples that remain in the sample pool.




## -see-also




<a href="https://msdn.microsoft.com/7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac">IMFVideoSampleAllocatorCallback</a>
 

 

