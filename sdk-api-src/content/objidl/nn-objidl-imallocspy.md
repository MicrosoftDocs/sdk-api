---
UID: NN:objidl.IMallocSpy
title: IMallocSpy (objidl.h)
author: windows-sdk-content
description: Enables application developers to monitor (spy on) memory allocation, detect memory leaks, and simulate memory failure in calls to IMalloc methods.
old-location: com\imallocspy.htm
tech.root: com
ms.assetid: 8ba500f7-c070-4788-b7fe-58b6a4e6a94c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMallocSpy, IMallocSpy interface [COM], IMallocSpy interface [COM],described, _com_imallocspy, com.imallocspy, objidl/IMallocSpy
ms.topic: interface
f1_keywords: ["objidl/IMallocSpy"]
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
ms.custom: 19H1
---

# IMallocSpy interface


## -description


Enables application developers to monitor (spy on) memory allocation, detect memory leaks, and simulate memory failure in calls to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> methods.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMallocSpy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMallocSpy</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-postalloc">PostAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-postdidalloc">PostDidAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-postfree">PostFree</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-postgetsize">PostGetSize</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-postheapminimize">PostHeapMinimize</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-heapminimize">IMalloc::HeapMinimize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-postrealloc">PostRealloc</a>
</td>
<td align="left" width="63%">
Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-prealloc">PreAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-predidalloc">PreDidAlloc</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-prefree">PreFree</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-pregetsize">PreGetSize</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-preheapminimize">PreHeapMinimize</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-heapminimize">IMalloc::HeapMinimize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-prerealloc">PreRealloc</a>
</td>
<td align="left" width="63%">
Performs operations required before calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-corevokemallocspy">CoRevokeMallocSpy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
 

 

