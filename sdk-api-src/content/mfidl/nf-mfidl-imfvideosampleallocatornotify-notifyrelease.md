---
UID: NF:mfidl.IMFVideoSampleAllocatorNotify.NotifyRelease
title: IMFVideoSampleAllocatorNotify::NotifyRelease (mfidl.h)
author: windows-sdk-content
description: Called when a video sample is returned to the allocator.
old-location: mf\imfvideosampleallocatornotify_notifyrelease.htm
tech.root: medfound
ms.assetid: 0467ebbe-b00d-41c1-8f50-77ca09337b15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorNotify interface [Media Foundation],NotifyRelease method, IMFVideoSampleAllocatorNotify.NotifyRelease, IMFVideoSampleAllocatorNotify::NotifyRelease, IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],NotifyRelease method, IMFVideoSampleAllocatorNotifyEx::NotifyRelease, NotifyRelease, NotifyRelease method [Media Foundation], NotifyRelease method [Media Foundation],IMFVideoSampleAllocatorNotify interface, NotifyRelease method [Media Foundation],IMFVideoSampleAllocatorNotifyEx interface, mf.imfvideosampleallocatornotify_notifyrelease, mfidl/IMFVideoSampleAllocatorNotify::NotifyRelease, mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyRelease
ms.topic: method
f1_keywords: 
 - "mfidl/IMFVideoSampleAllocatorNotify.NotifyRelease"
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
 - IMFVideoSampleAllocatorNotify.NotifyRelease
 - IMFVideoSampleAllocatorNotifyEx.NotifyRelease
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocatorNotify::NotifyRelease


## -description


Called when a video sample is returned to the allocator.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get a video sample from the allocator, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-allocatesample">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released and then returned to the pool of available samples, the allocator invokes the <b>NotifyRelease</b> method. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify">IMFVideoSampleAllocatorNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex">IMFVideoSampleAllocatorNotifyEx</a>
 

 

