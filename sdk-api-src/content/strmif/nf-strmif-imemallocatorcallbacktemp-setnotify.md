---
UID: NF:strmif.IMemAllocatorCallbackTemp.SetNotify
title: IMemAllocatorCallbackTemp::SetNotify
author: windows-sdk-content
description: The SetNotify method sets or removes a callback on the allocator. The allocator calls the callback method whenever the allocator's IMemAllocator::ReleaseBuffer method is called.
old-location: dshow\imemallocatorcallbacktemp_setnotify.htm
tech.root: DirectShow
ms.assetid: 70e885d6-8b8d-479f-a3c5-095446dfc58e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMemAllocatorCallbackTemp interface [DirectShow],SetNotify method, IMemAllocatorCallbackTemp.SetNotify, IMemAllocatorCallbackTemp::SetNotify, IMemAllocatorCallbackTempSetNotify, SetNotify, SetNotify method [DirectShow], SetNotify method [DirectShow],IMemAllocatorCallbackTemp interface, dshow.imemallocatorcallbacktemp_setnotify, strmif/IMemAllocatorCallbackTemp::SetNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IMemAllocatorCallbackTemp.SetNotify
: 
---

# IMemAllocatorCallbackTemp::SetNotify


## -description



The <code>SetNotify</code> method sets or removes a callback on the allocator. The allocator calls the callback method whenever the allocator's <a href="https://msdn.microsoft.com/96e02a28-af92-41a7-8251-c4ab15190651">IMemAllocator::ReleaseBuffer</a> method is called.




## -parameters




### -param pNotify

Pointer to the <a href="https://msdn.microsoft.com/63097b58-8197-4354-8b92-25baaf265df2">IMemAllocatorNotifyCallbackTemp</a> interface that will be used for the callback. The caller must implement the interface. Use the value <b>NULL</b> to remove the callback.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



Whenever the allocator's <b>ReleaseBuffer</b> method is called, the allocator calls the <b>NotifyRelease</b> method on the interface provided in <i>pNotify</i>. The <b>ReleaseBuffer</b> method returns a media sample to the allocator's free list. Samples call this method when their reference counts reach zero.

The allocator holds a reference count on the caller's <b>IMemAllocatorNotifyCallbackTemp</b> interface. This can create circular reference counts, thereby preventing objects in the graph from being released correctly. Therefore, when the caller no longer needs callback notifications, it should call this method again with the value <b>NULL</b>. An appropriate time to do this is when the graph stops, or else when the pins are disconnected.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6213faaa-86ff-46e7-80da-a043cae40805">IMemAllocatorCallbackTemp Interface</a>
 

 

