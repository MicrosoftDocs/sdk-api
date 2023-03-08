---
UID: NF:mfidl.IMFVideoSampleAllocatorNotifyEx.NotifyPrune
title: IMFVideoSampleAllocatorNotifyEx::NotifyPrune (mfidl.h)
description: Called when allocator samples are released for pruning by the allocator, or when the allocator is removed.
helpviewer_keywords: ["IMFVideoSampleAllocatorNotifyEx interface [Media Foundation]","NotifyPrune method","IMFVideoSampleAllocatorNotifyEx.NotifyPrune","IMFVideoSampleAllocatorNotifyEx::NotifyPrune","NotifyPrune","NotifyPrune method [Media Foundation]","NotifyPrune method [Media Foundation]","IMFVideoSampleAllocatorNotifyEx interface","mf.imfvideosampleallocatornotifyex_notifyprune","mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyPrune"]
old-location: mf\imfvideosampleallocatornotifyex_notifyprune.htm
tech.root: mf
ms.assetid: DCC3B043-4BD9-4A39-AA4C-98054223769F
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],NotifyPrune method, IMFVideoSampleAllocatorNotifyEx.NotifyPrune, IMFVideoSampleAllocatorNotifyEx::NotifyPrune, NotifyPrune, NotifyPrune method [Media Foundation], NotifyPrune method [Media Foundation],IMFVideoSampleAllocatorNotifyEx interface, mf.imfvideosampleallocatornotifyex_notifyprune, mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyPrune
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoSampleAllocatorNotifyEx::NotifyPrune
 - mfidl/IMFVideoSampleAllocatorNotifyEx::NotifyPrune
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
 - IMFVideoSampleAllocatorNotifyEx.NotifyPrune
---

# IMFVideoSampleAllocatorNotifyEx::NotifyPrune


## -description

Called when allocator samples are released for pruning by the allocator, or when the allocator is removed.

## -parameters

### -param __MIDL__IMFVideoSampleAllocatorNotifyEx0000

The sample to be pruned.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex">IMFVideoSampleAllocatorNotifyEx</a>