---
UID: NF:mfidl.IMFVideoSampleAllocatorNotify.NotifyRelease
title: IMFVideoSampleAllocatorNotify::NotifyRelease (mfidl.h)
description: Called when a video sample is returned to the allocator.
helpviewer_keywords: ["IMFVideoSampleAllocatorNotify interface [Media Foundation]","NotifyRelease method","IMFVideoSampleAllocatorNotify.NotifyRelease","IMFVideoSampleAllocatorNotify::NotifyRelease","IMFVideoSampleAllocatorNotifyEx interface [Media Foundation]","NotifyRelease method","IMFVideoSampleAllocatorNotifyEx::NotifyRelease","NotifyRelease","NotifyRelease method [Media Foundation]","NotifyRelease method [Media Foundation]","IMFVideoSampleAllocatorNotify interface","NotifyRelease method [Media Foundation]","IMFVideoSampleAllocatorNotifyEx interface","mf.imfvideosampleallocatornotify_notifyrelease","mfidl/IMFVideoSampleAllocatorNotify::NotifyRelease","mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyRelease"]
old-location: mf\imfvideosampleallocatornotify_notifyrelease.htm
tech.root: mf
ms.assetid: 0467ebbe-b00d-41c1-8f50-77ca09337b15
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorNotify interface [Media Foundation],NotifyRelease method, IMFVideoSampleAllocatorNotify.NotifyRelease, IMFVideoSampleAllocatorNotify::NotifyRelease, IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],NotifyRelease method, IMFVideoSampleAllocatorNotifyEx::NotifyRelease, NotifyRelease, NotifyRelease method [Media Foundation], NotifyRelease method [Media Foundation],IMFVideoSampleAllocatorNotify interface, NotifyRelease method [Media Foundation],IMFVideoSampleAllocatorNotifyEx interface, mf.imfvideosampleallocatornotify_notifyrelease, mfidl/IMFVideoSampleAllocatorNotify::NotifyRelease, mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyRelease
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
 - IMFVideoSampleAllocatorNotify::NotifyRelease
 - mfidl/IMFVideoSampleAllocatorNotify::NotifyRelease
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
 - IMFVideoSampleAllocatorNotify.NotifyRelease
 - IMFVideoSampleAllocatorNotifyEx.NotifyRelease
---

# IMFVideoSampleAllocatorNotify::NotifyRelease


## -description

Called when a video sample is returned to the allocator.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get a video sample from the allocator, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-allocatesample">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released and then returned to the pool of available samples, the allocator invokes the <b>NotifyRelease</b> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify">IMFVideoSampleAllocatorNotify</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex">IMFVideoSampleAllocatorNotifyEx</a>
