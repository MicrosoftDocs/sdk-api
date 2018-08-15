---
UID: NN:mfidl.IMFVideoSampleAllocatorNotify
title: IMFVideoSampleAllocatorNotify
author: windows-sdk-content
description: The callback for the IMFVideoSampleAllocatorCallback interface.
old-location: mf\imfvideosampleallocatornotify.htm
old-project: medfound
ms.assetid: 909c2a68-81dd-4816-b34f-71a67b620faf
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFVideoSampleAllocatorNotify, IMFVideoSampleAllocatorNotify interface [Media Foundation], IMFVideoSampleAllocatorNotify interface [Media Foundation],described, mf.imfvideosampleallocatornotify, mfidl/IMFVideoSampleAllocatorNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
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
 - IMFVideoSampleAllocatorNotify
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoSampleAllocatorNotify interface


## -description


The callback for the <a href="https://msdn.microsoft.com/7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac">IMFVideoSampleAllocatorCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoSampleAllocatorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoSampleAllocatorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0467ebbe-b00d-41c1-8f50-77ca09337b15">NotifyRelease</a>
</td>
<td align="left" width="63%">
Called when a video sample is returned to the allocator.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

