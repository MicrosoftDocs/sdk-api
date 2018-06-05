---
UID: NN:strmif.IMemAllocatorNotifyCallbackTemp
title: IMemAllocatorNotifyCallbackTemp
author: windows-sdk-content
description: Enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.
old-location: dshow\imemallocatornotifycallbacktemp.htm
old-project: DirectShow
ms.assetid: 63097b58-8197-4354-8b92-25baaf265df2
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMemAllocatorNotifyCallbackTemp, IMemAllocatorNotifyCallbackTemp interface [DirectShow], IMemAllocatorNotifyCallbackTemp interface [DirectShow],described, IMemAllocatorNotifyCallbackTempInterface, dshow.imemallocatornotifycallbacktemp, strmif/IMemAllocatorNotifyCallbackTemp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMemAllocatorNotifyCallbackTemp
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemAllocatorNotifyCallbackTemp interface


## -description


<p class="CCE_Message">[<b>IMemAllocatorNotifyCallbackTemp</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

The <b>IMemAllocatorNotifyCallbackTemp</b> interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list. To receive callbacks, the filter must implement this interface. For more information, see <a href="https://msdn.microsoft.com/6213faaa-86ff-46e7-80da-a043cae40805">IMemAllocatorCallbackTemp Interface</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemAllocatorNotifyCallbackTemp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMemAllocatorNotifyCallbackTemp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemAllocatorNotifyCallbackTemp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/deb5d97c-67f7-48ae-b408-1af89477b1b7">NotifyRelease</a>
</td>
<td align="left" width="63%">
Called when a sample returns to the allocator's free list.

</td>
</tr>
</table> 

