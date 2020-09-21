---
UID: NN:mfidl.IMFVideoSampleAllocatorNotifyEx
title: IMFVideoSampleAllocatorNotifyEx (mfidl.h)
description: The callback for the IMFVideoSampleAllocatorCallback interface.
helpviewer_keywords: ["IMFVideoSampleAllocatorNotifyEx","IMFVideoSampleAllocatorNotifyEx interface [Media Foundation]","IMFVideoSampleAllocatorNotifyEx interface [Media Foundation]","described","mf.imfvideosampleallocatornotifyex","mfidl/IMFVideoSampleAllocatorNotifyEx"]
old-location: mf\imfvideosampleallocatornotifyex.htm
tech.root: mf
ms.assetid: 5B3EA486-A45F-4C7B-8E36-80C9C2FD64F2
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorNotifyEx, IMFVideoSampleAllocatorNotifyEx interface [Media Foundation], IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],described, mf.imfvideosampleallocatornotifyex, mfidl/IMFVideoSampleAllocatorNotifyEx
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
 - IMFVideoSampleAllocatorNotifyEx
 - mfidl/IMFVideoSampleAllocatorNotifyEx
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
 - IMFVideoSampleAllocatorNotifyEx
---

# IMFVideoSampleAllocatorNotifyEx interface


## -description

The callback for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback">IMFVideoSampleAllocatorCallback</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorNotifyEx</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify">IMFVideoSampleAllocatorNotify</a>. <b>IMFVideoSampleAllocatorNotifyEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoSampleAllocatorNotifyEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatornotify-notifyrelease">IMFVideoSampleAllocatorNotify::NotifyRelease</a>
</td>
<td align="left" width="63%">
Called when a video sample is returned to the allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatornotifyex-notifyprune">NotifyPrune</a>
</td>
<td align="left" width="63%">
Called when allocator samples are released for pruning by the allocator, or when the allocator is removed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify">IMFVideoSampleAllocatorNotify</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>