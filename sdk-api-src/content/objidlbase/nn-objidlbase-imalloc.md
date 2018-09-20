---
UID: NN:objidlbase.IMalloc
title: IMalloc
author: windows-sdk-content
description: Allocates, frees, and manages memory.
old-location: com\imalloc.htm
tech.root: com
ms.assetid: 047f281e-2665-4d6d-9a0b-918cd3339447
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMalloc, IMalloc interface [COM], IMalloc interface [COM],described, _com_imalloc, com.imalloc, objidlbase/IMalloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - IMalloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMalloc interface


## -description


Allocates, frees, and manages memory.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMalloc</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IMalloc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMalloc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a>
</td>
<td align="left" width="63%">
Allocates a block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>
</td>
<td align="left" width="63%">
Determines whether this allocator was used to allocate the specified block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">Free</a>
</td>
<td align="left" width="63%">
Frees a previously allocated block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of a previously allocated block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b57e32eb-a637-47d8-b136-05cb193e9f73">HeapMinimize</a>
</td>
<td align="left" width="63%">
Minimizes the heap as much as possible by releasing unused memory to the operating system, coalescing adjacent free blocks, and committing free pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">Realloc</a>
</td>
<td align="left" width="63%">
Changes the size of a previously allocated block of memory.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>



<a href="https://msdn.microsoft.com/28623c1f-e158-4cc5-8c7f-c13d7a65aa76">CoRegisterMallocSpy</a>



<a href="https://msdn.microsoft.com/e1e984a2-2aee-452c-840c-42201ef5ee96">CoRevokeMallocSpy</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>
 

 

