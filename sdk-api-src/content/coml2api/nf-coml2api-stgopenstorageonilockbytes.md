---
UID: NF:coml2api.StgOpenStorageOnILockBytes
title: StgOpenStorageOnILockBytes function
author: windows-sdk-content
description: The StgOpenStorageOnILockBytes function opens an existing storage object that does not reside in a disk file, but instead has an underlying byte array provided by the caller.
old-location: stg\stgopenstorageonilockbytes.htm
old-project: stg
ms.assetid: 7920bd46-0a8f-42e0-9988-59d85edb64e2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: StgOpenStorageOnILockBytes, StgOpenStorageOnILockBytes function [Structured Storage], _stg_stgopenstorageonilockbytes, coml2api/StgOpenStorageOnILockBytes, stg.stgopenstorageonilockbytes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: coml2api.h
req.include-header: Objbase.h
req.redist: 
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - StgOpenStorageOnILockBytes
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# StgOpenStorageOnILockBytes function


## -description


The <b>StgOpenStorageOnILockBytes</b> function opens an existing storage object that does not reside in a disk file, but instead has an underlying byte array provided by the caller.


## -parameters




### -param plkbyt [in]


<a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> pointer to the underlying byte array object that contains the storage object to be opened.


### -param pstgPriority [in]

A pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface that should be <b>NULL</b>. If not <b>NULL</b>, this parameter is used as described below in the Remarks section.

After <b>StgOpenStorageOnILockBytes</b> returns, the storage object specified in <i>pStgPriority</i> may have been released and should no longer be used.


### -param grfMode [in]

Specifies the access mode to use to open the storage object. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa380337(v=VS.85).aspx">STGM Constants</a> and the Remarks section below. 


### -param snbExclude [in]

Can be <b>NULL</b>. If not <b>NULL</b>, this parameter points to a block of elements in this storage that are to be excluded as the storage object is opened. This exclusion occurs independently of whether a snapshot copy happens on the open.


### -param reserved [in]

Indicates reserved for future use; must be zero.


### -param ppstgOpen [out]

Points to the location of an 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> pointer to the opened storage on successful return.


## -returns



The <b>StgOpenStorageOnILockBytes</b> function can also return any file system errors, or system errors wrapped in an <b>HRESULT</b>, or 
<a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> interface error return values. See 
<a href="https://msdn.microsoft.com/en-us/library/ms688560(v=VS.85).aspx">Error Handling Strategies</a> 
and 
<a href="https://msdn.microsoft.com/en-us/library/ms693442(v=VS.85).aspx">Handling Unknown Errors</a>.




## -remarks



<b>StgOpenStorageOnILockBytes</b> opens the specified root storage object. A pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface on the opened storage object is supplied through the <i>ppstgOpen</i> parameter.

The storage object must have been previously created by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380324(v=VS.85).aspx">StgCreateDocfileOnILockBytes</a> function.

Except for specifying a programmer-provided byte-array object, 
<b>StgOpenStorageOnILockBytes</b> is similar to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380341(v=VS.85).aspx">StgOpenStorage</a> function. The storage object is opened according to the access modes in the <i>grfMode</i> parameter, subject to the following restrictions:

Sharing mode behavior and transactional isolation depend on the <a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> implementation supporting <a href="https://msdn.microsoft.com/en-us/library/Aa379242(v=VS.85).aspx">LockRegion</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa379250(v=VS.85).aspx">UnlockRegion</a> with <a href="https://msdn.microsoft.com/en-us/library/Aa380048(v=VS.85).aspx">LOCK_ONLYONCE</a> semantics.  Implementations can indicate to structured storage they support this functionality by setting the <b>LOCK_ONLYONCE</b> bit in the <b>grfLocksSupported</b> member of <a href="https://msdn.microsoft.com/en-us/library/Aa380319(v=VS.85).aspx">STATSTG</a>.  If an <b>ILockBytes</b> implementation does not support this functionality, sharing modes will not be enforced, and root-level transactional commits will not coordinate properly with other transactional instances opened on the same byte array.  Applications that use an <b>ILockBytes</b> implementation that does not support region locking, such as the <a href="https://msdn.microsoft.com/en-us/library/Aa378980(v=VS.85).aspx">CreateStreamOnHGlobal</a> implementation, should avoid opening multiple concurrent instances on the same byte array.

<b>StgOpenStorageOnILockBytes</b> does not support simple mode.  The <a href="https://msdn.microsoft.com/en-us/library/Aa380337(v=VS.85).aspx">STGM_SIMPLE</a> flag, if present, is ignored. 

The  <i>pStgPriority</i> parameter is intended as a convenience for callers replacing an existing storage object, often one opened in priority mode, with a new storage object opened on the same byte array. Unlike the <i>pStgPriority</i> parameter of <a href="https://msdn.microsoft.com/en-us/library/Aa380341(v=VS.85).aspx">StgOpenStorage</a>, this parameter does not affect the open operation performed by <b>StgOpenStorageOnILockBytes</b> and is simply an existing storage object the caller would like released.  Callers should always pass <b>NULL</b> for this parameter because <b>StgOpenStorageOnILockBytes</b> releases the object under some circumstances, and does not release it under other circumstances.
The use of the <i>pStgPriority</i> parameter can be duplicated by the caller in a safer manner by instead releasing the object before calling <b>StgOpenStorageOnILockBytes</b>, as shown in the following example:

<pre class="syntax" xml:space="preserve"><code>// Replacement for:
// HRESULT hr = StgOpenStorageOnILockBytes(
//         plkbyt, pStgPriority, grfMode, NULL, 0, &amp;pstgNew);

pStgPriority-&gt;Release();
pStgPriority = NULL;
hr = StgOpenStorage(plkbyt, NULL, grfMode, NULL, 0, &amp;pstgNew);
    
</code></pre>
For more information, refer to 
<a href="https://msdn.microsoft.com/en-us/library/Aa380341(v=VS.85).aspx">StgOpenStorage</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380324(v=VS.85).aspx">StgCreateDocfileOnILockBytes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380341(v=VS.85).aspx">StgOpenStorage</a>
 

 

