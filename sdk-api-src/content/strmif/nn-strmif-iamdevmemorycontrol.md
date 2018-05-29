---
UID: NN:strmif.IAMDevMemoryControl
title: IAMDevMemoryControl
author: windows-sdk-content
description: Note  This interface is no longer supported by the AVI Splitter. Note  It was defined to support certain older hardware decoders that required AVI files to be read directly into hardware memory.
old-location: dshow\iamdevmemorycontrol.htm
old-project: DirectShow
ms.assetid: 9945bffb-6748-4c7d-ba14-91470cf6c651
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IAMDevMemoryControl, IAMDevMemoryControl interface [DirectShow], IAMDevMemoryControl interface [DirectShow],described, IAMDevMemoryControlInterface, dshow.iamdevmemorycontrol, strmif/IAMDevMemoryControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmif.h
api_name:
-	IAMDevMemoryControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDevMemoryControl interface


## -description



<div class="alert"><b>Note</b>  This interface is no longer supported by the AVI Splitter.</div>
<div> </div>
<div class="alert"><b>Note</b>  It was defined to support certain older hardware decoders that required AVI files to be read directly into hardware memory. The interface enables the AVI parser to allocate memory from the downstream filter but still provide its own allocator. There should be no need for any newer devices to support this interface.</div>
<div> </div>
A device memory control object supports <code>IAMDevMemoryControl</code>. This object is aggregated with an <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> object that is used in the connection. Typically, filters will call the <a href="https://msdn.microsoft.com/d7ca361a-1ce6-449f-9d81-fbfe39f0f9f0">IAMDevMemoryAllocator::GetDevMemoryObject</a> method to obtain a pointer to this interface.

Implement this interface with the <a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator</a> interface when pins need to have greater control of memory allocation.

Use this interface to synchronize the completion of writing data to a memory allocator, and to get the device ID of the on-board memory allocator.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDevMemoryControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMDevMemoryControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDevMemoryControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/398cc4b3-c025-4df4-8447-bd4599293dab">GetDevId</a>
</td>
<td align="left" width="63%">
Retrieves the device ID of the on-board memory allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec6dd7e2-b1f2-48fa-bf79-2688e286425e">QueryWriteSync</a>
</td>
<td align="left" width="63%">
Checks if the memory supported by the allocator requires the use of the <b>WriteSync</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46bf7ab6-cc3c-4846-a8f8-97c62ede4aaf">WriteSync</a>
</td>
<td align="left" width="63%">
Used to synchronize with the completed write operation by returning when any data being written to the specified allocator region is fully written into the memory.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

