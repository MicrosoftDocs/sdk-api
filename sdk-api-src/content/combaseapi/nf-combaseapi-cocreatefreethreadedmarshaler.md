---
UID: NF:combaseapi.CoCreateFreeThreadedMarshaler
title: CoCreateFreeThreadedMarshaler function (combaseapi.h)
author: windows-sdk-content
description: Creates an aggregatable object capable of context-dependent marshaling.
old-location: com\cocreatefreethreadedmarshaler.htm
tech.root: com
ms.assetid: f97a2a39-7291-4a1d-b770-0a34f7f5b60f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoCreateFreeThreadedMarshaler, CoCreateFreeThreadedMarshaler function [COM], _com_CoCreateFreeThreadedMarshaler, com.cocreatefreethreadedmarshaler, combaseapi/CoCreateFreeThreadedMarshaler
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoCreateFreeThreadedMarshaler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoCreateFreeThreadedMarshaler function


## -description


Creates an aggregatable object capable of context-dependent marshaling.


## -parameters




### -param punkOuter [in]

A pointer to the aggregating object's controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>.


### -param ppunkMarshal [out]

Address of the pointer variable that receives the interface pointer to the aggregatable marshaler.


## -returns



This function can return the standard return value E_OUTOFMEMORY, as well as the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The marshaler was created.

</td>
</tr>
</table>
 




## -remarks



The <b>CoCreateFreeThreadedMarshaler</b> function enables an object to efficiently marshal interface pointers between threads in the same process. If your objects do not support interthread marshaling, you have no need to call this function. It is intended for use by free-threaded DLL servers that must be accessed directly by all threads in a process, even those threads associated with single-threaded apartments. It custom-marshals the real memory pointer over into other apartments as a bogus "proxy" and thereby gives direct access to all callers, even if they are not free-threaded.

The <b>CoCreateFreeThreadedMarshaler</b> function performs the following tasks: 



<ol>
<li>Creates a free-threaded marshaler object.</li>
<li>Aggregates this marshaler to the object specified by the <i>punkOuter</i> parameter. This object is normally the one whose interface pointers are to be marshaled.</li>
</ol>
The aggregating object's implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> should delegate <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> calls for IID_IMarshal to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the free-threaded marshaler. Upon receiving a call, the free-threaded marshaler performs the following tasks: 



<ol>
<li>Checks the destination context specified by the <a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a> function's <i>dwDestContext</i> parameter.</li>
<li>If the destination context is MSHCTX_INPROC, copies the interface pointer into the marshaling stream.</li>
<li>If the destination context is any other value, finds or creates an instance of COM's default (standard) marshaler and delegates marshaling to it.
</li>
</ol>
Values for <i>dwDestContext</i> come from the <a href="https://msdn.microsoft.com/d7d09ab2-96e7-48da-9292-0e4ca6cebe64">MSHCTX</a> enumeration. MSHCTX_INPROC indicates that the interface pointer is to be marshaled between different threads in the same process. Because both threads have access to the same address space, the client thread can dereference the pointer directly rather than having to direct calls to a proxy. In all other cases, a proxy is required, so <b>CoCreateFreeThreadedMarshaler</b> delegates the marshaling job to COM's default implementation.



Great care should be exercised in using the <b>CoCreateFreeThreadedMarshaler</b> function. This is because the performance of objects which aggregate the free-threaded marshaler is obtained through a calculated violation of the rules of COM, with the ever-present risk of undefined behavior unless the object operates within certain restrictions. The most important restrictions are:

<ul>
<li>A free-threaded marshaler object cannot hold direct pointers to interfaces on an object that does not aggregate the free-threaded marshaler as part of its state. If the object were to use direct references to ordinary single-threaded aggregate objects, it may break their single threaded property. If the object were to use direct references to ordinary multithreaded aggregate objects, these objects can behave in ways that show no sensitivity to the needs of direct single-threaded aggregate clients. For example, these objects can spin new threads and pass parameters to the threads that are references to ordinary single-threaded aggregate objects.
</li>
<li>A free-threaded marshaler object cannot hold references to proxies to objects in other apartments. Proxies are sensitive to the threading model and can return RPC_E_WRONG_THREAD if called by the wrong client.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b529f65f-3208-4594-a772-d1cad3727dc1">CoGetInterfaceAndReleaseStream</a>



<a href="https://msdn.microsoft.com/c9ab8713-8604-4f0b-a11b-bdfb7d595d95">CoMarshalInterThreadInterfaceInStream</a>
 

 

