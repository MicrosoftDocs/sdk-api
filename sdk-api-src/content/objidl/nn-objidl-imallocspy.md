---
UID: NN:objidl.IMallocSpy
title: IMallocSpy
author: windows-sdk-content
description: Enables application developers to monitor (spy on) memory allocation, detect memory leaks, and simulate memory failure in calls to IMalloc methods.
old-location: com\imallocspy.htm
tech.root: com
ms.assetid: 8ba500f7-c070-4788-b7fe-58b6a4e6a94c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMallocSpy, IMallocSpy interface [COM], IMallocSpy interface [COM],described, _com_imallocspy, com.imallocspy, objidl/IMallocSpy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidl.h
req.include-header: 
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
 - ObjIdl.h
api_name:
 - IMallocSpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMallocSpy interface


## -description


Enables application developers to monitor (spy on) memory allocation, detect memory leaks, and simulate memory failure in calls to <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> methods.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMallocSpy</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IMallocSpy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMallocSpy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaf2cb92-afdb-4f1f-a46a-83b6c72db07f">PostAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/820ff316-9edd-4894-8461-fc532d439348">PostDidAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b46b0b1e-6144-4bb8-84d5-9db5690b7421">PostFree</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac619736-a434-46c0-9874-0cb646fdecae">PostGetSize</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d51c34e-6ed1-493d-8999-e67c4a60f6b6">PostHeapMinimize</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://msdn.microsoft.com/b57e32eb-a637-47d8-b136-05cb193e9f73">IMalloc::HeapMinimize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77f86494-f7b3-4c12-bb42-ad74161a1dff">PostRealloc</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43d8223b-a3fb-432c-ab4e-009d79ad8658">PreAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f18b6dba-c0fe-40c2-835b-01dff521d27c">PreDidAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/528eedac-e8cc-4dc7-8287-c023ebefb72c">PreFree</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bebc327-490e-4a41-8043-5d7211e645f5">PreGetSize</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e80f555-5382-4bd9-ab56-a67f42b13cae">PreHeapMinimize</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://msdn.microsoft.com/b57e32eb-a637-47d8-b136-05cb193e9f73">IMalloc::HeapMinimize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd4db69c-3369-4aca-bc05-4c3c6850cc09">PreRealloc</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>



<a href="https://msdn.microsoft.com/28623c1f-e158-4cc5-8c7f-c13d7a65aa76">CoRegisterMallocSpy</a>



<a href="https://msdn.microsoft.com/e1e984a2-2aee-452c-840c-42201ef5ee96">CoRevokeMallocSpy</a>



<a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a>
 

 

