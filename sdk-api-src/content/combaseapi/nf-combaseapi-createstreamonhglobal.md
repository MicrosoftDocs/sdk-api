---
UID: NF:combaseapi.CreateStreamOnHGlobal
title: CreateStreamOnHGlobal function (combaseapi.h)
description: Creates a stream object that uses an HGLOBAL memory handle to store the stream contents.
helpviewer_keywords: ["CreateStreamOnHGlobal","CreateStreamOnHGlobal function [Structured Storage]","_stg_createstreamonhglobal","combaseapi/CreateStreamOnHGlobal","stg.createstreamonhglobal"]
old-location: stg\createstreamonhglobal.htm
tech.root: Stg
ms.assetid: 413c107b-a943-4c02-9c00-aea708e876d7
ms.date: 12/05/2018
ms.keywords: CreateStreamOnHGlobal, CreateStreamOnHGlobal function [Structured Storage], _stg_createstreamonhglobal, combaseapi/CreateStreamOnHGlobal, stg.createstreamonhglobal
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateStreamOnHGlobal
 - combaseapi/CreateStreamOnHGlobal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CreateStreamOnHGlobal
---

# CreateStreamOnHGlobal function


## -description

The <b>CreateStreamOnHGlobal</b> function creates a stream object that uses an HGLOBAL memory handle to store the stream contents. This object is the OLE-provided implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

The returned stream object supports both reading and writing, is not transacted, and does not support region locking. The object calls the <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function to grow the memory block as required.


<div class="alert"><b>Tip</b>  Consider using the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatememstream">SHCreateMemStream</a> function, which produces better performance, or for Windows Store apps, consider using <a href="/uwp/api/windows.storage.streams.inmemoryrandomaccessstream">InMemoryRandomAccessStream</a>.</div>
<div> </div>

## -parameters

### -param hGlobal [in]

A memory handle allocated by the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function, or if <b>NULL</b> a new handle is to be allocated instead. The handle must be allocated as moveable and nondiscardable.

### -param fDeleteOnRelease [in]

A value that indicates whether the underlying handle for this stream object should be automatically freed when the stream object is released. If set to <b>FALSE</b>, the caller must free the <i>hGlobal</i> after the final release. If set to <b>TRUE</b>, the final release will automatically free the underlying handle. See the Remarks for further discussion of the case where <i>fDeleteOnRelease</i> is <b>FALSE</b>.

### -param ppstm [out]

The address of 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>* pointer variable that receives the interface pointer to the new stream object. Its value cannot be <b>NULL</b>.

## -returns

This function supports the standard return values E_INVALIDARG and E_OUTOFMEMORY, as well as the following.

## -remarks

If <i>hGlobal</i> is <b>NULL</b>, the function allocates a new memory handle and the stream is initially empty.

If <i>hGlobal</i> is not <b>NULL</b>, the initial contents of the stream are the current contents of the memory block. Thus, <b>CreateStreamOnHGlobal</b> can be used to open an existing stream in memory. The memory handle and its contents are undisturbed by the creation of the new stream object.

The initial size of the stream is the size of <i>hGlobal</i> as returned by the <a href="/windows/desktop/api/winbase/nf-winbase-globalsize">GlobalSize</a> function. Because of rounding, this is not necessarily the same size that was originally allocated for the handle. If the logical size of the stream is important, follow the call to this function with a call to the 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-setsize">IStream::SetSize</a> method.

The new stream object’s initial seek position is the beginning of the stream.

After creating the stream object with 
<b>CreateStreamOnHGlobal</b>, call 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream">GetHGlobalFromStream</a> to retrieve the memory handle associated with the stream object.

If a memory handle is passed to  <b>CreateStreamOnHGlobal</b> or if <a href="/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream">GetHGlobalFromStream</a> is called, the memory handle of this function can be directly accessed by the caller while it is still in use by the stream object. Appropriate caution should be exercised in the use of this capability and its implications:

<ul>
<li>Do not free the <i>hGlobal</i> memory handle during the lifetime of the stream object. <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IStream::Release</a> must be called before freeing the memory handle.</li>
<li>Do not call <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> to change the size of the memory handle during the lifetime of the stream object or its clones.  This may cause application crashes or memory corruption. Avoid creating multiple stream objects separately on the same memory handle, because the <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">IStream::Write</a> and <a href="/windows/desktop/api/objidl/nf-objidl-istream-setsize">IStream::SetSize</a> methods may internally call <b>GlobalReAlloc</b>.  The <a href="/windows/desktop/api/objidl/nf-objidl-istream-clone">IStream::Clone</a> method can be used to create a new stream object based on the same memory handle that will properly coordinate its access with the original stream object.</li>
<li>If possible, avoid accessing the memory block during the lifetime of the stream object, because the object may internally call <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> and do not make assumptions about its size and location.  If the memory block must be accessed, the memory access calls should be surrounded by calls to <a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> and <a href="/windows/desktop/api/winbase/nf-winbase-globalunlock">GlobalUnLock</a>.</li>
<li>Avoid calling the object’s methods while you have the memory handle locked with <a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>.  This can cause method calls to fail unpredictably.</li>
</ul>
If the <i>fDeleteOnRelease</i> parameter is <b>FALSE</b>, the caller is responsible for freeing the underlying memory handle, even if the <i>hGlobal</i> parameter is <b>NULL</b>. Use the <b>GetHGlobalFromStream</b> function to obtain the underlying memory handle and <b>GlobalFree</b> that memory after the last reference to the stream is released. If the caller sets the <i>fDeleteOnRelease</i> parameter to <b>TRUE</b>, the final release will automatically free the underlying memory handle.

The memory handle passed as the <i>hGlobal</i> parameter must be allocated as movable and nondiscardable, as shown in the following example:


```cpp
HGLOBAL	hMem = ::GlobalAlloc(GMEM_MOVEABLE,iSize);
if (!hMem)
    AfxThrowMemoryException();

LPVOID pImage = ::GlobalLock(hMem);
... // Fill memory
::GlobalUnlock(hMem);

CComPtr<IStream> spStream;
HRESULT hr = ::CreateStreamOnHGlobal(hMem,FALSE,&spStream);
```


<b>CreateStreamOnHGlobal</b> will accept a memory handle allocated with <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GMEM_FIXED</a>, but this usage is not recommended. HGLOBALs allocated with <b>GMEM_FIXED</b> are not really handles and their value can change when they are reallocated. If the memory handle was allocated with <b>GMEM_FIXED</b> and <i>fDeleteOnRelease</i> is <b>FALSE</b>,  the caller must call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream">GetHGlobalFromStream</a> to get the correct handle in order to free it.

Prior to Windows 7 and Windows Server 2008 R2, this implementation did not zero memory when calling <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> to grow the memory block. Increasing the size of the stream with <a href="/windows/desktop/api/objidl/nf-objidl-istream-setsize">IStream::SetSize</a> or by writing to a location past the current end of the stream may leave portions of the newly allocated memory uninitialized.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream">GetHGlobalFromStream</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istream-setsize">IStream::SetSize</a>



<a href="/uwp/api/windows.storage.streams.inmemoryrandomaccessstream">InMemoryRandomAccessStream</a>
