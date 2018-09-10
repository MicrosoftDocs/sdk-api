---
UID: NN:mfidl.IMFVideoSampleAllocator
title: IMFVideoSampleAllocator
author: windows-sdk-content
description: Allocates video samples for a video media sink.
old-location: mf\imfvideosampleallocator.htm
tech.root: medfound
ms.assetid: bef92133-ae6c-4013-9210-5e0f0be2002c
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFVideoSampleAllocator, IMFVideoSampleAllocator interface [Media Foundation], IMFVideoSampleAllocator interface [Media Foundation],described, bef92133-ae6c-4013-9210-5e0f0be2002c, mf.imfvideosampleallocator, mfidl/IMFVideoSampleAllocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoSampleAllocator interface


## -description


Allocates video samples for a video media sink.

The stream sinks on the enhanced video renderer (EVR) expose this interface as a service. To obtain a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> using the service identifier MR_VIDEO_ACCELERATION_SERVICE. Custom media sinks can also implement this interface. The Media Session uses this interface to allocate samples for the EVR, unless the upstream decoder supports DirectX Video Acceleration (DXVA).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoSampleAllocator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e5347cef-edbd-4f6a-88c9-042e53515a32">AllocateSample</a>
</td>
<td align="left" width="63%">
Gets a video sample from the allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1e4557e-990c-4239-b9ec-5c7c46072e54">InitializeSampleAllocator</a>
</td>
<td align="left" width="63%">
Specifies the number of samples to allocate and the media type for the samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bad810c9-f5b1-42dc-9c7a-3306f3de2846">SetDirectXManager</a>
</td>
<td align="left" width="63%">
Specifies the Direct3D device manager for the video media sink to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bcb0425-00ac-4fdc-83a8-2b2686979a1d">UninitializeSampleAllocator</a>
</td>
<td align="left" width="63%">
Releases all of the video samples that have been allocated.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

