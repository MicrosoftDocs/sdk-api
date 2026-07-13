---
UID: NF:mfidl.IMFVideoSampleAllocatorCallback.SetCallback
title: IMFVideoSampleAllocatorCallback::SetCallback (mfidl.h)
description: Sets the callback object that receives notification whenever a video sample is returned to the allocator.
helpviewer_keywords: ["IMFVideoSampleAllocatorCallback interface [Media Foundation]","SetCallback method","IMFVideoSampleAllocatorCallback.SetCallback","IMFVideoSampleAllocatorCallback::SetCallback","SetCallback","SetCallback method [Media Foundation]","SetCallback method [Media Foundation]","IMFVideoSampleAllocatorCallback interface","mf.imfvideosampleallocatorcallback_setcallback","mfidl/IMFVideoSampleAllocatorCallback::SetCallback"]
old-location: mf\imfvideosampleallocatorcallback_setcallback.htm
tech.root: mf
ms.assetid: edcf1ef2-d71f-4ca1-94db-ebf358e80e57
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorCallback interface [Media Foundation],SetCallback method, IMFVideoSampleAllocatorCallback.SetCallback, IMFVideoSampleAllocatorCallback::SetCallback, SetCallback, SetCallback method [Media Foundation], SetCallback method [Media Foundation],IMFVideoSampleAllocatorCallback interface, mf.imfvideosampleallocatorcallback_setcallback, mfidl/IMFVideoSampleAllocatorCallback::SetCallback
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
 - IMFVideoSampleAllocatorCallback::SetCallback
 - mfidl/IMFVideoSampleAllocatorCallback::SetCallback
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
 - IMFVideoSampleAllocatorCallback.SetCallback
---

# IMFVideoSampleAllocatorCallback::SetCallback


## -description

Sets the callback object that receives notification whenever a video sample is returned to the allocator.

## -parameters

### -param pNotify [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify">IMFVideoSampleAllocatorNotify</a> interface that receives notification, or <b>NULL</b> to remove the callback.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get a video sample from the allocator, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-allocatesample">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released, it returns to the pool of available samples. When this happens, the allocator invokes the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatornotify-notifyrelease">IMFVideoSampleAllocatorNotify::NotifyRelease</a> callback.

The allocator holds at most one callback pointer. Calling this method again replaces the previous callback pointer.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback">IMFVideoSampleAllocatorCallback</a>