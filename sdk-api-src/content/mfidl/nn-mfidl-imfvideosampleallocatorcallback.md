---
UID: NN:mfidl.IMFVideoSampleAllocatorCallback
title: IMFVideoSampleAllocatorCallback
author: windows-sdk-content
description: Enables an application to track video samples allocated by the enhanced video renderer (EVR).
old-location: mf\imfvideosampleallocatorcallback.htm
tech.root: medfound
ms.assetid: 7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFVideoSampleAllocatorCallback, IMFVideoSampleAllocatorCallback interface [Media Foundation], IMFVideoSampleAllocatorCallback interface [Media Foundation],described, mf.imfvideosampleallocatorcallback, mfidl/IMFVideoSampleAllocatorCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoSampleAllocatorCallback interface


## -description


Enables an application to track video samples allocated by the enhanced video renderer (EVR).

The stream sinks on the EVR expose this interface as a service. To get a pointer to the interface, call the <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> method, using the <b>MR_VIDEO_ACCELERATION_SERVICE</b> service identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoSampleAllocatorCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0025067b-1c8f-4f1a-91f2-edf6a274523b">GetFreeSampleCount</a>
</td>
<td align="left" width="63%">
Gets the number of video samples that are currently available for use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edcf1ef2-d71f-4ca1-94db-ebf358e80e57">SetCallback</a>
</td>
<td align="left" width="63%">
Sets the  callback object that receives notification whenever a video sample is returned to the allocator.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bef92133-ae6c-4013-9210-5e0f0be2002c">IMFVideoSampleAllocator</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

