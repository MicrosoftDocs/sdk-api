---
UID: NN:strmif.IMemAllocatorCallbackTemp
title: IMemAllocatorCallbackTemp
author: windows-sdk-content
description: The IMemAllocatorCallbackTemp interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.The use of this interface is deprecated.
old-location: dshow\imemallocatorcallbacktemp.htm
tech.root: DirectShow
ms.assetid: 6213faaa-86ff-46e7-80da-a043cae40805
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMemAllocatorCallbackTemp, IMemAllocatorCallbackTemp interface [DirectShow], IMemAllocatorCallbackTemp interface [DirectShow],described, IMemAllocatorCallbackTempInterface, dshow.imemallocatorcallbacktemp, strmif/IMemAllocatorCallbackTemp
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
 - IMemAllocatorCallbackTemp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMemAllocatorCallbackTemp interface


## -description



The <code>IMemAllocatorCallbackTemp</code> interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.

The use of this interface is deprecated.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemAllocatorCallbackTemp</b> interface inherits from <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a>. <b>IMemAllocatorCallbackTemp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemAllocatorCallbackTemp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2dd0cdb3-664a-4022-b8bb-fda759172dd6">GetFreeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of free media samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70e885d6-8b8d-479f-a3c5-095446dfc58e">SetNotify</a>
</td>
<td align="left" width="63%">
Sets or removes a callback on the allocator.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a>
 

 

