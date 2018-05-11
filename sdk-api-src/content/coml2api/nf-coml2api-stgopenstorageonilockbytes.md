---
UID: NF:coml2api.StgOpenStorageOnILockBytes
title: StgOpenStorageOnILockBytes function
author: windows-driver-content
description: The StgOpenStorageOnILockBytes function opens an existing storage object that does not reside in a disk file, but instead has an underlying byte array provided by the caller.
old-location: stg\stgopenstorageonilockbytes.htm
old-project: Stg
ms.assetid: 7920bd46-0a8f-42e0-9988-59d85edb64e2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: StgOpenStorageOnILockBytes, StgOpenStorageOnILockBytes function [Structured Storage], _stg_stgopenstorageonilockbytes, coml2api/StgOpenStorageOnILockBytes, stg.stgopenstorageonilockbytes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	Ext-MS-Win-COM-OLE32-l1-1-0.dll
-	Ext-MS-Win-COM-OLE32-l1-1-1.dll
-	Ext-MS-Win-COM-OLE32-l1-1-2.dll
-	ext-ms-win-com-ole32-l1-1-3.dll
-	API-MS-Win-Core-Com-l2-1-1.dll
-	coml2.dll
-	Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
-	StgOpenStorageOnILockBytes
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


<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> pointer to the underlying byte array object that contains the storage object to be opened.


### -param pstgPriority

TBD


### -param grfMode [in]

Specifies the access mode to use to open the storage object. For more information, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a> and the Remarks section below. 


### -param snbExclude [in]

Can be <b>NULL</b>. If not <b>NULL</b>, this parameter points to a block of elements in this storage that are to be excluded as the storage object is opened. This exclusion occurs independently of whether a snapshot copy happens on the open.


### -param reserved [in]

Indicates reserved for future use; must be zero.


### -param ppstgOpen [out]

Points to the location of an 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the opened storage on successful return.


#### - pStgPriority [in]

A pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface that should be <b>NULL</b>. If not <b>NULL</b>, this parameter is used as described below in the Remarks section.

After <b>StgOpenStorageOnILockBytes</b> returns, the storage object specified in <i>pStgPriority</i> may have been released and should no longer be used.


## -returns



The <b>StgOpenStorageOnILockBytes</b> function can also return any file system errors, or system errors wrapped in an <b>HRESULT</b>, or 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface error return values. See 
<a href="_com_error_handling_strategies">Error Handling Strategies</a> 
and 
<a href="_com_handling_unknown_errors">Handling Unknown Errors</a>.




## -remarks



<b>StgOpenStorageOnILockBytes</b> opens the specified root storage object. A pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the opened storage object is supplied through the <i>ppstgOpen</i> parameter.

The storage object must have been previously created by the 
<a href="https://msdn.microsoft.com/8af5098d-db04-4273-8f5f-6d1a1d9541de">StgCreateDocfileOnILockBytes</a> function.

Except for specifying a programmer-provided byte-array object, 
<b>StgOpenStorageOnILockBytes</b> is similar to the 
<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a> function. The storage object is opened according to the access modes in the <i>grfMode</i> parameter, subject to the following restrictions:

Sharing mode behavior and transactional isolation depend on the <a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> implementation supporting <a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">LockRegion</a> and <a href="https://msdn.microsoft.com/036ba242-8630-4013-860d-dd37919253be">UnlockRegion</a> with <a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCK_ONLYONCE</a> semantics.  Implementations can indicate to structured storage they support this functionality by setting the <b>LOCK_ONLYONCE</b> bit in the <b>grfLocksSupported</b> member of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>.  If an <b>ILockBytes</b> implementation does not support this functionality, sharing modes will not be enforced, and root-level transactional commits will not coordinate properly with other transactional instances opened on the same byte array.  Applications that use an <b>ILockBytes</b> implementation that does not support region locking, such as the <a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a> implementation, should avoid opening multiple concurrent instances on the same byte array.

<b>StgOpenStorageOnILockBytes</b> does not support simple mode.  The <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM_SIMPLE</a> flag, if present, is ignored. 

The  <i>pStgPriority</i> parameter is intended as a convenience for callers replacing an existing storage object, often one opened in priority mode, with a new storage object opened on the same byte array. Unlike the <i>pStgPriority</i> parameter of <a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>, this parameter does not affect the open operation performed by <b>StgOpenStorageOnILockBytes</b> and is simply an existing storage object the caller would like released.  Callers should always pass <b>NULL</b> for this parameter because <b>StgOpenStorageOnILockBytes</b> releases the object under some circumstances, and does not release it under other circumstances.
The use of the <i>pStgPriority</i> parameter can be duplicated by the caller in a safer manner by instead releasing the object before calling <b>StgOpenStorageOnILockBytes</b>, as shown in the following example:

<pre class="syntax" xml:space="preserve"><code>// Replacement for:
// HRESULT hr = StgOpenStorageOnILockBytes(
//         plkbyt, pStgPriority, grfMode, NULL, 0, &amp;pstgNew);

pStgPriority-&gt;Release();
pStgPriority = NULL;
hr = StgOpenStorage(plkbyt, NULL, grfMode, NULL, 0, &amp;pstgNew);
    
</code></pre>
For more information, refer to 
<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>.




## -see-also




<a href="https://msdn.microsoft.com/8af5098d-db04-4273-8f5f-6d1a1d9541de">StgCreateDocfileOnILockBytes</a>



<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>
 

 

