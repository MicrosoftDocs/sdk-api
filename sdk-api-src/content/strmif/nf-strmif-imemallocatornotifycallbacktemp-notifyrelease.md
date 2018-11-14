---
UID: NF:strmif.IMemAllocatorNotifyCallbackTemp.NotifyRelease
title: IMemAllocatorNotifyCallbackTemp::NotifyRelease
author: windows-sdk-content
description: The NotifyRelease method is called whenever the allocator's IMemAllocator::ReleaseBuffer method is called. The ReleaseBuffer method returns a media sample to the allocator's free list. Samples call this method when their reference counts reach zero.
old-location: dshow\imemallocatornotifycallbacktemp_notifyrelease.htm
tech.root: DirectShow
ms.assetid: deb5d97c-67f7-48ae-b408-1af89477b1b7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMemAllocatorNotifyCallbackTemp interface [DirectShow],NotifyRelease method, IMemAllocatorNotifyCallbackTemp.NotifyRelease, IMemAllocatorNotifyCallbackTemp::NotifyRelease, IMemAllocatorNotifyCallbackTempNotifyRelease, NotifyRelease, NotifyRelease method [DirectShow], NotifyRelease method [DirectShow],IMemAllocatorNotifyCallbackTemp interface, dshow.imemallocatornotifycallbacktemp_notifyrelease, strmif/IMemAllocatorNotifyCallbackTemp::NotifyRelease
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
 - IMemAllocatorNotifyCallbackTemp.NotifyRelease
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
- IMemAllocatorNotifyCallbackTemp.NotifyRelease
: 
---

# IMemAllocatorNotifyCallbackTemp::NotifyRelease


## -description



The <code>NotifyRelease</code> method is called whenever the allocator's <a href="https://msdn.microsoft.com/96e02a28-af92-41a7-8251-c4ab15190651">IMemAllocator::ReleaseBuffer</a> method is called. The <b>ReleaseBuffer</b> method returns a media sample to the allocator's free list. Samples call this method when their reference counts reach zero.




## -parameters






## -returns



Return S_OK or an error code.




## -remarks



In general, this call can occur on any thread, and the caller may be holding critical sections. Therefore, this method should not do anything that could cause a deadlock. Instead, the method should set an event or post a message to another thread, and the other thread should take any required actions.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/63097b58-8197-4354-8b92-25baaf265df2">IMemAllocatorNotifyCallbackTemp Interface</a>
 

 

