---
UID: NF:coml2api.CreateILockBytesOnHGlobal
title: CreateILockBytesOnHGlobal function (coml2api.h)
description: Creates a byte array object that uses an HGLOBAL memory handle to store the bytes intended for in-memory storage of a compound file.
helpviewer_keywords: ["CreateILockBytesOnHGlobal","CreateILockBytesOnHGlobal function [Structured Storage]","_stg_createilockbytesonhglobal","coml2api/CreateILockBytesOnHGlobal","stg.createilockbytesonhglobal"]
old-location: stg\createilockbytesonhglobal.htm
tech.root: Stg
ms.assetid: e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c
ms.date: 12/05/2018
ms.keywords: CreateILockBytesOnHGlobal, CreateILockBytesOnHGlobal function [Structured Storage], _stg_createilockbytesonhglobal, coml2api/CreateILockBytesOnHGlobal, stg.createilockbytesonhglobal
req.header: coml2api.h
req.include-header: Ole2.h
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
 - CreateILockBytesOnHGlobal
 - coml2api/CreateILockBytesOnHGlobal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - CreateILockBytesOnHGlobal
---

# CreateILockBytesOnHGlobal function


## -description

The <b>CreateILockBytesOnHGlobal</b> function creates a byte array object that uses an HGLOBAL memory handle to store the bytes intended for in-memory storage of a compound file. This object is the OLE-provided implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface.

The returned byte array object supports both reading and writing, but does not support region locking .  The object calls the <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function to grow the memory block as required.

## -parameters

### -param hGlobal [in]

A memory handle allocated by the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function, or if <b>NULL</b> a new handle is to be allocated instead. The handle must be allocated as moveable and nondiscardable.

### -param fDeleteOnRelease [in]

A flag  that specifies whether the underlying handle for this byte array object should be automatically freed when the object is released. If set to <b>FALSE</b>, the caller must free the <i>hGlobal</i> after the final release. If set to <b>TRUE</b>, the final release will automatically free the <i>hGlobal</i> parameter.

### -param pplkbyt [out]

The address of 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> pointer variable that receives the interface pointer to the new byte array object.

## -returns

This function supports the standard return values <b>E_INVALIDARG</b> and <b>E_OUTOFMEMORY</b>, as well as the following:

## -remarks

If <i>hGlobal</i> is <b>NULL</b>, the <b>CreateILockBytesOnHGlobal</b> allocates a new memory handle and the byte array is empty initially.

If <i>hGlobal</i> is not <b>NULL</b>, the initial contents of the byte array object are the current contents of the memory block. Thus, this function can be used to open an existing byte array in memory, for example to reload a storage object previously created by the <a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes">StgCreateDocfileOnILockBytes</a> function. The memory handle and its contents are undisturbed by the creation of the new byte array object.

The initial size of the byte array is the size of <i>hGlobal</i> as returned by the <a href="/windows/desktop/api/winbase/nf-winbase-globalsize">GlobalSize</a> function. This is not necessarily the same size that was originally allocated for the handle because of rounding. If the logical size of the byte array is important, follow the call to <b>CreateILockBytesOnHGlobal</b> with a call to <a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-setsize">ILockBytes::SetSize</a>.

After creating the byte array object with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a>, <a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes">StgCreateDocfileOnILockBytes</a> can be used to create a new storage object in memory, or <a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes">StgOpenStorageOnILockBytes</a> can be used to reopen a previously existing storage object that is already contained in the memory block. <a href="/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes">GetHGlobalFromILockBytes</a> can be called to retrieve the memory handle associated with the byte array object.

If a memory handle is passed to <b>CreateILockBytesOnHGlobal</b> or if <a href="/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes">GetHGlobalFromILockBytes</a> is called, the memory handle of this function can be directly accessed by the caller while it is still in use by the byte array object.  Appropriate caution should be exercised in the use of this capability and its implications:

<ul>
<li>Do not free the <i>hGlobal</i> memory handle during the lifetime of the byte array object. <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">ILockBytes::Release</a> must be called before the memory handle is freed.</li>
<li>Do not call <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> to change the size of the memory handle during the lifetime of the byte array object.  This may cause application crashes or memory corruption. Avoid creating multiple byte array objects on the same memory handle, because <a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-writeat">ILockBytes::WriteAt</a> and <a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-setsize">ILockBytes::SetSize</a> methods may internally call <b>GlobalReAlloc</b>.</li>
<li>If possible, avoid accessing the memory block during the lifetime of the byte array object, because the object may internally call <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> and do not make assumptions about its size and location.  If the memory block must be accessed, the memory access calls should be surrounded by calls to <a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> and <a href="/windows/desktop/api/winbase/nf-winbase-globalunlock">GlobalUnLock</a>.</li>
<li>Avoid calling the object’s methods while the memory handle is locked with <a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>.  This can cause method calls to fail unpredictably.</li>
</ul>
If the caller sets the <i>fDeleteOnRelease</i> parameter to <b>FALSE</b>, then the caller must also free the <i>hGlobal</i> after the final release. If the caller sets the <i>fDeleteOnRelease</i> parameter to <b>TRUE</b>, the final release will automatically free the <i>hGlobal</i>. The memory handle passed as the hGlobal parameter must be allocated as movable and nondiscardable, as shown in the following example:


```cpp
HGLOBAL	hMem = ::GlobalAlloc(GMEM_MOVEABLE,iSize);
if (!hMem)
    AfxThrowMemoryException();

LPVOID pCompoundFile = ::GlobalLock(hMem);
... // Fill memory
::GlobalUnlock(hMem);

CComPtr<ILockBytes> spLockBytes;
HRESULT hr = ::CreateILockBytesOnHGlobal(hMem,FALSE,&spLockBytes);


```


<b>CreateILockBytesOnHGlobal</b> will accept memory allocated with <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GMEM_FIXED</a>, but this usage is not recommended. HGLOBALs allocated with <b>GMEM_FIXED</b> are not really handles and their value can change when they are reallocated. If the memory handle was allocated with <b>GMEM_FIXED</b> and <i>fDeleteOnRelease</i> is <b>FALSE</b>, then the caller must call <a href="/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes">GetHGlobalFromILockBytes</a> to get the correct HGLOBAL value in order to free the handle.

This implementation of <a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> does not support region locking.  Applications that use this implementation with the <a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes">StgCreateDocfileOnILockBytes</a> or <a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes">StgOpenStorageOnILockBytes</a> functions should avoid opening multiple concurrent instances on the same <b>ILockBytes</b> object. 

Prior to Windows 7 and Windows Server 2008 R2, this implementation did not zero memory when calling <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> to grow the memory block. Increasing the size of the byte array with <a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-setsize">ILockBytes::SetSize</a> or by writing to a location past the current end of the byte array will leave any unwritten portions of the newly allocated memory uninitialized. The storage objects returned by the <a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes">StgCreateDocfileOnILockBytes</a> and <a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes">StgOpenStorageOnILockBytes</a> may increase the size of the byte array without initializing all of the newly allocated space.

Compound files in memory are typically used as scratch space or with APIs that require a storage object, and in these cases the uninitialized memory is generally not a concern. However, if the contents of the memory block will be written to a file, consider the following alternatives to avoid potential information disclosure:<ul>
<li>Copy the logical contents of the in-memory compound file to the destination file using the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-copyto">IStorage::CopyTo</a> method rather than directly writing the contents of the memory block.</li>
<li>Instead of a compound file in memory, create a temporary file by calling <a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex">StgCreateStorageEx</a> with a <b>NULL</b> value for the <i>pwcsName</i> parameter. When it is time to write to the destination file, use the <a href="/windows/desktop/api/objidl/nf-objidl-irootstorage-switchtofile">IRootStorage::SwitchToFile</a> method.</li>
<li>Implement the <a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface such that memory reallocations are zeroed (see for example the <b>HEAP_ZERO_MEMORY</b> flag in <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a>). The memory contents of this byte array can then be written to a file. </li>
</ul>

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes">GetHGlobalFromILockBytes</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes">StgOpenStorageOnILockBytes</a>