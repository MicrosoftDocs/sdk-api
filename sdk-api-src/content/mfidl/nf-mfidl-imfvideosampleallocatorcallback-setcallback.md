---
UID: NF:mfidl.IMFVideoSampleAllocatorCallback.SetCallback
title: IMFVideoSampleAllocatorCallback::SetCallback
author: windows-sdk-content
description: Sets the callback object that receives notification whenever a video sample is returned to the allocator.
old-location: mf\imfvideosampleallocatorcallback_setcallback.htm
old-project: medfound
ms.assetid: edcf1ef2-d71f-4ca1-94db-ebf358e80e57
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFVideoSampleAllocatorCallback interface [Media Foundation],SetCallback method, IMFVideoSampleAllocatorCallback.SetCallback, IMFVideoSampleAllocatorCallback::SetCallback, SetCallback, SetCallback method [Media Foundation], SetCallback method [Media Foundation],IMFVideoSampleAllocatorCallback interface, mf.imfvideosampleallocatorcallback_setcallback, mfidl/IMFVideoSampleAllocatorCallback::SetCallback
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
 - IMFVideoSampleAllocatorCallback.SetCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoSampleAllocatorCallback::SetCallback


## -description


Sets the callback object that receives notification whenever a video sample is returned to the allocator.


## -parameters




### -param pNotify [in]

A pointer to the <a href="https://msdn.microsoft.com/909c2a68-81dd-4816-b34f-71a67b620faf">IMFVideoSampleAllocatorNotify</a> interface that receives notification, or <b>NULL</b> to remove the callback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get a video sample from the allocator, call the <a href="https://msdn.microsoft.com/e5347cef-edbd-4f6a-88c9-042e53515a32">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released, it returns to the pool of available samples. When this happens, the allocator invokes the <a href="https://msdn.microsoft.com/0467ebbe-b00d-41c1-8f50-77ca09337b15">IMFVideoSampleAllocatorNotify::NotifyRelease</a> callback.

The allocator holds at most one callback pointer. Calling this method again replaces the previous callback pointer.




## -see-also




<a href="https://msdn.microsoft.com/7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac">IMFVideoSampleAllocatorCallback</a>
 

 

