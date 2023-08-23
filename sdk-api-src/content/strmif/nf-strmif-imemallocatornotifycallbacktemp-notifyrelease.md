---
UID: NF:strmif.IMemAllocatorNotifyCallbackTemp.NotifyRelease
title: IMemAllocatorNotifyCallbackTemp::NotifyRelease (strmif.h)
description: The NotifyRelease method is called whenever the allocator's IMemAllocator::ReleaseBuffer method is called. The ReleaseBuffer method returns a media sample to the allocator's free list. Samples call this method when their reference counts reach zero.
helpviewer_keywords: ["IMemAllocatorNotifyCallbackTemp interface [DirectShow]","NotifyRelease method","IMemAllocatorNotifyCallbackTemp.NotifyRelease","IMemAllocatorNotifyCallbackTemp::NotifyRelease","IMemAllocatorNotifyCallbackTempNotifyRelease","NotifyRelease","NotifyRelease method [DirectShow]","NotifyRelease method [DirectShow]","IMemAllocatorNotifyCallbackTemp interface","dshow.imemallocatornotifycallbacktemp_notifyrelease","strmif/IMemAllocatorNotifyCallbackTemp::NotifyRelease"]
old-location: dshow\imemallocatornotifycallbacktemp_notifyrelease.htm
tech.root: dshow
ms.assetid: deb5d97c-67f7-48ae-b408-1af89477b1b7
ms.date: 4/26/2023
ms.keywords: IMemAllocatorNotifyCallbackTemp interface [DirectShow],NotifyRelease method, IMemAllocatorNotifyCallbackTemp.NotifyRelease, IMemAllocatorNotifyCallbackTemp::NotifyRelease, IMemAllocatorNotifyCallbackTempNotifyRelease, NotifyRelease, NotifyRelease method [DirectShow], NotifyRelease method [DirectShow],IMemAllocatorNotifyCallbackTemp interface, dshow.imemallocatornotifycallbacktemp_notifyrelease, strmif/IMemAllocatorNotifyCallbackTemp::NotifyRelease
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMemAllocatorNotifyCallbackTemp::NotifyRelease
 - strmif/IMemAllocatorNotifyCallbackTemp::NotifyRelease
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocatorNotifyCallbackTemp.NotifyRelease
---

# IMemAllocatorNotifyCallbackTemp::NotifyRelease


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NotifyRelease</code> method is called whenever the allocator's <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-releasebuffer">IMemAllocator::ReleaseBuffer</a> method is called. The <b>ReleaseBuffer</b> method returns a media sample to the allocator's free list. Samples call this method when their reference counts reach zero.



## -returns

Return S_OK or an error code.

## -remarks

In general, this call can occur on any thread, and the caller may be holding critical sections. Therefore, this method should not do anything that could cause a deadlock. Instead, the method should set an event or post a message to another thread, and the other thread should take any required actions.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocatornotifycallbacktemp">IMemAllocatorNotifyCallbackTemp Interface</a>
