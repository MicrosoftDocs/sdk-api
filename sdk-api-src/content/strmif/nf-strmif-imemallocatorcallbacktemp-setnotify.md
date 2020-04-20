---
UID: NF:strmif.IMemAllocatorCallbackTemp.SetNotify
title: IMemAllocatorCallbackTemp::SetNotify (strmif.h)
description: The SetNotify method sets or removes a callback on the allocator. The allocator calls the callback method whenever the allocator's IMemAllocator::ReleaseBuffer method is called.helpviewer_keywords: ["IMemAllocatorCallbackTemp interface [DirectShow]","SetNotify method","IMemAllocatorCallbackTemp.SetNotify","IMemAllocatorCallbackTemp::SetNotify","IMemAllocatorCallbackTempSetNotify","SetNotify","SetNotify method [DirectShow]","SetNotify method [DirectShow]","IMemAllocatorCallbackTemp interface","dshow.imemallocatorcallbacktemp_setnotify","strmif/IMemAllocatorCallbackTemp::SetNotify"]
old-location: dshow\imemallocatorcallbacktemp_setnotify.htm
tech.root: DirectShow
ms.assetid: 70e885d6-8b8d-479f-a3c5-095446dfc58e
ms.date: 12/05/2018
ms.keywords: IMemAllocatorCallbackTemp interface [DirectShow],SetNotify method, IMemAllocatorCallbackTemp.SetNotify, IMemAllocatorCallbackTemp::SetNotify, IMemAllocatorCallbackTempSetNotify, SetNotify, SetNotify method [DirectShow], SetNotify method [DirectShow],IMemAllocatorCallbackTemp interface, dshow.imemallocatorcallbacktemp_setnotify, strmif/IMemAllocatorCallbackTemp::SetNotify
f1_keywords:
- strmif/IMemAllocatorCallbackTemp.SetNotify
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMemAllocatorCallbackTemp.SetNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemAllocatorCallbackTemp::SetNotify


## -description



The <code>SetNotify</code> method sets or removes a callback on the allocator. The allocator calls the callback method whenever the allocator's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-releasebuffer">IMemAllocator::ReleaseBuffer</a> method is called.




## -parameters




### -param pNotify

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocatornotifycallbacktemp">IMemAllocatorNotifyCallbackTemp</a> interface that will be used for the callback. The caller must implement the interface. Use the value <b>NULL</b> to remove the callback.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



Whenever the allocator's <b>ReleaseBuffer</b> method is called, the allocator calls the <b>NotifyRelease</b> method on the interface provided in <i>pNotify</i>. The <b>ReleaseBuffer</b> method returns a media sample to the allocator's free list. Samples call this method when their reference counts reach zero.

The allocator holds a reference count on the caller's <b>IMemAllocatorNotifyCallbackTemp</b> interface. This can create circular reference counts, thereby preventing objects in the graph from being released correctly. Therefore, when the caller no longer needs callback notifications, it should call this method again with the value <b>NULL</b>. An appropriate time to do this is when the graph stops, or else when the pins are disconnected.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocatorcallbacktemp">IMemAllocatorCallbackTemp Interface</a>
 

 

