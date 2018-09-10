---
UID: NN:mfidl.IMFVideoSampleAllocatorNotifyEx
title: IMFVideoSampleAllocatorNotifyEx
author: windows-sdk-content
description: The callback for the IMFVideoSampleAllocatorCallback interface.
old-location: mf\imfvideosampleallocatornotifyex.htm
tech.root: medfound
ms.assetid: 5B3EA486-A45F-4C7B-8E36-80C9C2FD64F2
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFVideoSampleAllocatorNotifyEx, IMFVideoSampleAllocatorNotifyEx interface [Media Foundation], IMFVideoSampleAllocatorNotifyEx interface [Media Foundation],described, mf.imfvideosampleallocatornotifyex, mfidl/IMFVideoSampleAllocatorNotifyEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMFVideoSampleAllocatorNotifyEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoSampleAllocatorNotifyEx interface


## -description


The callback for the <a href="https://msdn.microsoft.com/7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac">IMFVideoSampleAllocatorCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorNotifyEx</b> interface inherits from <a href="https://msdn.microsoft.com/909c2a68-81dd-4816-b34f-71a67b620faf">IMFVideoSampleAllocatorNotify</a>. <b>IMFVideoSampleAllocatorNotifyEx</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0467ebbe-b00d-41c1-8f50-77ca09337b15">IMFVideoSampleAllocatorNotify::NotifyRelease</a>
</td>
<td align="left" width="63%">
Called when a video sample is returned to the allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DCC3B043-4BD9-4A39-AA4C-98054223769F">NotifyPrune</a>
</td>
<td align="left" width="63%">
Called when allocator samples are released for pruning by the allocator, or when the allocator is removed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/909c2a68-81dd-4816-b34f-71a67b620faf">IMFVideoSampleAllocatorNotify</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

