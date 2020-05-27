---
UID: NN:mfidl.IMFVideoSampleAllocator
title: IMFVideoSampleAllocator (mfidl.h)
description: Allocates video samples for a video media sink.
helpviewer_keywords: ["IMFVideoSampleAllocator","IMFVideoSampleAllocator interface [Media Foundation]","IMFVideoSampleAllocator interface [Media Foundation]","described","bef92133-ae6c-4013-9210-5e0f0be2002c","mf.imfvideosampleallocator","mfidl/IMFVideoSampleAllocator"]
old-location: mf\imfvideosampleallocator.htm
tech.root: medfound
ms.assetid: bef92133-ae6c-4013-9210-5e0f0be2002c
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocator, IMFVideoSampleAllocator interface [Media Foundation], IMFVideoSampleAllocator interface [Media Foundation],described, bef92133-ae6c-4013-9210-5e0f0be2002c, mf.imfvideosampleallocator, mfidl/IMFVideoSampleAllocator
f1_keywords:
- mfidl/IMFVideoSampleAllocator
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFVideoSampleAllocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocator interface


## -description


Allocates video samples for a video media sink.

The stream sinks on the enhanced video renderer (EVR) expose this interface as a service. To obtain a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> using the service identifier MR_VIDEO_ACCELERATION_SERVICE. Custom media sinks can also implement this interface. The Media Session uses this interface to allocate samples for the EVR, unless the upstream decoder supports DirectX Video Acceleration (DXVA).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoSampleAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoSampleAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-allocatesample">AllocateSample</a>
</td>
<td align="left" width="63%">
Gets a video sample from the allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-initializesampleallocator">InitializeSampleAllocator</a>
</td>
<td align="left" width="63%">
Specifies the number of samples to allocate and the media type for the samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-setdirectxmanager">SetDirectXManager</a>
</td>
<td align="left" width="63%">
Specifies the Direct3D device manager for the video media sink to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-uninitializesampleallocator">UninitializeSampleAllocator</a>
</td>
<td align="left" width="63%">
Releases all of the video samples that have been allocated.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

