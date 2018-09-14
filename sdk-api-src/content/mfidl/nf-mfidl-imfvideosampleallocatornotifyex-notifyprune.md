---
UID: NF:mfidl.IMFVideoSampleAllocatorNotifyEx.NotifyPrune
title: IMFVideoSampleAllocatorNotifyEx::NotifyPrune
author: windows-sdk-content
description: Called when allocator samples are released for pruning by the allocator, or when the allocator is removed.
old-location: mf\imfvideosampleallocatornotifyex_notifyprune.htm
tech.root: medfound
ms.assetid: DCC3B043-4BD9-4A39-AA4C-98054223769F
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],NotifyPrune method, IMFVideoSampleAllocatorNotifyEx.NotifyPrune, IMFVideoSampleAllocatorNotifyEx::NotifyPrune, NotifyPrune, NotifyPrune method [Media Foundation], NotifyPrune method [Media Foundation],IMFVideoSampleAllocatorNotifyEx interface, mf.imfvideosampleallocatornotifyex_notifyprune, mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyPrune
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
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
 - IMFVideoSampleAllocatorNotifyEx.NotifyPrune
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoSampleAllocatorNotifyEx::NotifyPrune


## -description


Called when allocator samples are released for pruning by the allocator, or when the allocator is removed.


## -parameters




### -param __MIDL__IMFVideoSampleAllocatorNotifyEx0000

TBD




#### - pSample

The sample to be pruned.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>



<a href="https://msdn.microsoft.com/5B3EA486-A45F-4C7B-8E36-80C9C2FD64F2">IMFVideoSampleAllocatorNotifyEx</a>
 

 

