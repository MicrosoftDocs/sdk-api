---
UID: NF:combaseapi.CreateStreamOnHGlobal
title: CreateStreamOnHGlobal function
author: windows-sdk-content
description: Creates a stream object that uses an HGLOBAL memory handle to store the stream contents.
old-location: stg\createstreamonhglobal.htm
old-project: stg
ms.assetid: 413c107b-a943-4c02-9c00-aea708e876d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateStreamOnHGlobal, CreateStreamOnHGlobal function [Structured Storage], _stg_createstreamonhglobal, combaseapi/CreateStreamOnHGlobal, stg.createstreamonhglobal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: 
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
tech.root: 
req.typenames: REGCLS
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
 - CreateStreamOnHGlobal
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CreateStreamOnHGlobal function


## -description


The 
<b>CreateStreamOnHGlobal</b>function creates a stream object that uses an HGLOBAL memory handle to store the stream contents. This object is the OLE-provided implementation of the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface.

The returned stream object supports both reading and writing, is not transacted, and does not support region locking. The object calls the <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function to grow the memory block as required.


<div class="alert"><b>Tip</b>  Consider using the <a href="https://msdn.microsoft.com/f3ae8241-f3a6-4007-a10f-ff05960c5de8">SHCreateMemStream</a> function, which produces better performance, or for Windows Store apps, consider using <a href="https://msdn.microsoft.com/5e11da69-8b7e-45da-8ab6-0a5ecd3808dc">InMemoryRandomAccessStream</a>.</div>
<div> </div>



## -parameters




### -param hGlobal [in]

A memory handle allocated by the <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> function, or if <b>NULL</b> a new handle is to be allocated instead. The handle must be allocated as moveable and nondiscardable.


### -param fDeleteOnRelease [in]

A value that indicates whether the underlying handle for this stream object should be automatically freed when the stream object is released. If set to <b>FALSE</b>, the caller must free the <i>hGlobal</i> after the final release. If set to <b>TRUE</b>, the final release will automatically free the <i>hGlobal</i> parameter.


### -param ppstm [out]

The address of 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>* pointer variable that receives the interface pointer to the new stream object. Its value cannot be <b>NULL</b>.


## -returns



This function supports the standard return values E_INVALIDARG and E_OUTOFMEMORY, as well as the following.




## -remarks



If <i>hGlobal</i> is <b>NULL</b>, the function allocates a new memory handle and the stream is initially empty.

If <i>hGlobal</i> is not <b>NULL</b>, the initial contents of the stream are the current contents of the memory block. Thus, <b>CreateStreamOnHGlobal</b> can be used to open an existing stream in memory. The memory handle and its contents are undisturbed by the creation of the new stream object.

The initial size of the stream is the size of <i>hGlobal</i> as returned by the <a href="https://msdn.microsoft.com/9fd01460-d6fc-41f4-9e0c-209a3d1844c1">GlobalSize</a> function. Because of rounding, this is not necessarily the same size that was originally allocated for the handle. If the logical size of the stream is important, follow the call to this function with a call to the 
<a href="https://msdn.microsoft.com/05627db5-067b-4a1a-a7ed-c83314f8bd8d">IStream::SetSize</a> method.

The new stream object’s initial seek position is the beginning of the stream.

After creating the stream object with 
<b>CreateStreamOnHGlobal</b>, call 
<a href="https://msdn.microsoft.com/79e39345-7a20-4b0f-bceb-f62de13d3260">GetHGlobalFromStream</a> to retrieve the memory handle associated with the stream object.

If a memory handle is passed to  <b>CreateStreamOnHGlobal</b> or if <a href="https://msdn.microsoft.com/79e39345-7a20-4b0f-bceb-f62de13d3260">GetHGlobalFromStream</a> is called, the memory handle of this function can be directly accessed by the caller while it is still in use by the stream object. Appropriate caution should be exercised in the use of this capability and its implications:

<ul>
<li>Do not free the <i>hGlobal</i> memory handle during the lifetime of the stream object. <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IStream::Release</a> must be called before freeing the memory handle.</li>
<li>Do not call <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> to change the size of the memory handle during the lifetime of the stream object or its clones.  This may cause application crashes or memory corruption. Avoid creating multiple stream objects separately on the same memory handle, because the <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">IStream::Write</a> and <a href="https://msdn.microsoft.com/05627db5-067b-4a1a-a7ed-c83314f8bd8d">IStream::SetSize</a> methods may internally call <b>GlobalReAlloc</b>.  The <a href="https://msdn.microsoft.com/677c37fb-598f-4bb0-b5d6-600e0befc722">IStream::Clone</a> method can be used to create a new stream object based on the same memory handle that will properly coordinate its access with the original stream object.</li>
<li>If possible, avoid accessing the memory block during the lifetime of the stream object, because the object may internally call <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> and do not make assumptions about its size and location.  If the memory block must be accessed, the memory access calls should be surrounded by calls to <a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a> and <a href="https://msdn.microsoft.com/580a2873-7f06-47a1-acf5-c2b3c96e15e7">GlobalUnLock</a>.</li>
<li>Avoid calling the object’s methods while you have the memory handle locked with <a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a>.  This can cause method calls to fail unpredictably.</li>
</ul>
If the caller sets the <i>fDeleteOnRelease</i> parameter to <b>FALSE</b>, then the caller must also free the <i>hGlobal</i> after the final release. If the caller sets the <i>fDeleteOnRelease</i> parameter to <b>TRUE</b>, the final release will automatically free the <i>hGlobal</i>.

The memory handle passed as the <i>hGlobal</i> parameter must be allocated as movable and nondiscardable, as shown in the following example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HGLOBAL	hMem = ::GlobalAlloc(GMEM_MOVEABLE,iSize);
if (!hMem)
    AfxThrowMemoryException();

LPVOID pImage = ::GlobalLock(hMem);
... // Fill memory
::GlobalUnlock(hMem);

CComPtr&lt;IStream&gt; spStream;
HRESULT hr = ::CreateStreamOnHGlobal(hMem,FALSE,&amp;spStream);</pre>
</td>
</tr>
</table></span></div>
<b>CreateStreamOnHGlobal</b> will accept a memory handle allocated with <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GMEM_FIXED</a>, but this usage is not recommended. HGLOBALs allocated with <b>GMEM_FIXED</b> are not really handles and their value can change when they are reallocated. If the memory handle was allocated with <b>GMEM_FIXED</b> and <i>fDeleteOnRelease</i> is <b>FALSE</b>,  the caller must call <a href="https://msdn.microsoft.com/79e39345-7a20-4b0f-bceb-f62de13d3260">GetHGlobalFromStream</a> to get the correct handle in order to free it.

Prior to Windows 7 and Windows Server 2008 R2, this implementation did not zero memory when calling <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> to grow the memory block. Increasing the size of the stream with <a href="https://msdn.microsoft.com/05627db5-067b-4a1a-a7ed-c83314f8bd8d">IStream::SetSize</a> or by writing to a location past the current end of the stream may leave portions of the newly allocated memory uninitialized.




## -see-also




<a href="https://msdn.microsoft.com/79e39345-7a20-4b0f-bceb-f62de13d3260">GetHGlobalFromStream</a>



<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/05627db5-067b-4a1a-a7ed-c83314f8bd8d">IStream::SetSize</a>



<a href="https://msdn.microsoft.com/80b4d7c9-f4a9-40ec-8dc4-9759d56646f2">InMemoryRandomAccessStream</a>
 

 

