---
UID: NN:mfidl.IMFVideoSampleAllocatorCallback
title: IMFVideoSampleAllocatorCallback (mfidl.h)
description: Enables an application to track video samples allocated by the enhanced video renderer (EVR).helpviewer_keywords: ["IMFVideoSampleAllocatorCallback","IMFVideoSampleAllocatorCallback interface [Media Foundation]","IMFVideoSampleAllocatorCallback interface [Media Foundation]","described","mf.imfvideosampleallocatorcallback","mfidl/IMFVideoSampleAllocatorCallback"]
old-location: mf\imfvideosampleallocatorcallback.htm
tech.root: medfound
ms.assetid: 7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorCallback, IMFVideoSampleAllocatorCallback interface [Media Foundation], IMFVideoSampleAllocatorCallback interface [Media Foundation],described, mf.imfvideosampleallocatorcallback, mfidl/IMFVideoSampleAllocatorCallback
f1_keywords:
- mfidl/IMFVideoSampleAllocatorCallback
dev_langs:
- c++
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
- IMFVideoSampleAllocatorCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocatorCallback interface


## -description


Enables an application to track video samples allocated by the enhanced video renderer (EVR).

The stream sinks on the EVR expose this interface as a service. To get a pointer to the interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> method, using the <b>MR_VIDEO_ACCELERATION_SERVICE</b> service identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoSampleAllocatorCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoSampleAllocatorCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorcallback-getfreesamplecount">GetFreeSampleCount</a>
</td>
<td align="left" width="63%">
Gets the number of video samples that are currently available for use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorcallback-setcallback">SetCallback</a>
</td>
<td align="left" width="63%">
Sets the  callback object that receives notification whenever a video sample is returned to the allocator.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

