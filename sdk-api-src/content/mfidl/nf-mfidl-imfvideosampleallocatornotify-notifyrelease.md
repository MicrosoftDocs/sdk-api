---
UID: NF:mfidl.IMFVideoSampleAllocatorNotify.NotifyRelease
title: IMFVideoSampleAllocatorNotify::NotifyRelease
author: windows-sdk-content
description: Called when a video sample is returned to the allocator.
old-location: mf\imfvideosampleallocatornotify_notifyrelease.htm
old-project: medfound
ms.assetid: 0467ebbe-b00d-41c1-8f50-77ca09337b15
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFVideoSampleAllocatorNotify interface [Media Foundation],NotifyRelease method, IMFVideoSampleAllocatorNotify.NotifyRelease, IMFVideoSampleAllocatorNotify::NotifyRelease, IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],NotifyRelease method, IMFVideoSampleAllocatorNotifyEx::NotifyRelease, NotifyRelease, NotifyRelease method [Media Foundation], NotifyRelease method [Media Foundation],IMFVideoSampleAllocatorNotify interface, NotifyRelease method [Media Foundation],IMFVideoSampleAllocatorNotifyEx interface, mf.imfvideosampleallocatornotify_notifyrelease, mfidl/IMFVideoSampleAllocatorNotify::NotifyRelease, mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyRelease
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoSampleAllocatorNotify::NotifyRelease


## -description


Called when a video sample is returned to the allocator.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get a video sample from the allocator, call the <a href="https://msdn.microsoft.com/e5347cef-edbd-4f6a-88c9-042e53515a32">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released and then returned to the pool of available samples, the allocator invokes the <b>NotifyRelease</b> method. 




## -see-also




<a href="https://msdn.microsoft.com/909c2a68-81dd-4816-b34f-71a67b620faf">IMFVideoSampleAllocatorNotify</a>



<a href="https://msdn.microsoft.com/5B3EA486-A45F-4C7B-8E36-80C9C2FD64F2">IMFVideoSampleAllocatorNotifyEx</a>
 

 

