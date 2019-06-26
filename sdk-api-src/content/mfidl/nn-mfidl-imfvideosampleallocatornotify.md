---
UID: NN:mfidl.IMFVideoSampleAllocatorNotify
title: IMFVideoSampleAllocatorNotify (mfidl.h)
author: windows-sdk-content
description: The callback for the IMFVideoSampleAllocatorCallback interface.
old-location: mf\imfvideosampleallocatornotify.htm
tech.root: medfound
ms.assetid: 909c2a68-81dd-4816-b34f-71a67b620faf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorNotify, IMFVideoSampleAllocatorNotify interface [Media Foundation], IMFVideoSampleAllocatorNotify interface [Media Foundation],described, mf.imfvideosampleallocatornotify, mfidl/IMFVideoSampleAllocatorNotify
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFVideoSampleAllocatorNotify"
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
 - IMFVideoSampleAllocatorNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocatorNotify interface


## -description


The callback for the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback">IMFVideoSampleAllocatorCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoSampleAllocatorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoSampleAllocatorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatornotify-notifyrelease">NotifyRelease</a>
</td>
<td align="left" width="63%">
Called when a video sample is returned to the allocator.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

