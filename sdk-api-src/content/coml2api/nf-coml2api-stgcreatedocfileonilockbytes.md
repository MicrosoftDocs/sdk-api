---
UID: NF:coml2api.StgCreateDocfileOnILockBytes
title: StgCreateDocfileOnILockBytes function
author: windows-sdk-content
description: Creates and opens a new compound file storage object on top of a byte-array object provided by the caller.
old-location: stg\stgcreatedocfileonilockbytes.htm
tech.root: Stg
ms.assetid: 8af5098d-db04-4273-8f5f-6d1a1d9541de
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: StgCreateDocfileOnILockBytes, StgCreateDocfileOnILockBytes function [Structured Storage], _stg_stgcreatedocfileonilockbytes, coml2api/StgCreateDocfileOnILockBytes, stg.stgcreatedocfileonilockbytes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
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
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgCreateDocfileOnILockBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StgCreateDocfileOnILockBytes function


## -description


The <b>StgCreateDocfileOnILockBytes</b> function creates and opens a new compound file storage object on top of a byte-array object provided by the caller. The storage object supports the COM-provided, compound-file implementation for the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface.


## -parameters




### -param plkbyt [in]

A pointer to the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface on the underlying byte-array object on which to create a compound file.


### -param grfMode [in]

Specifies the access mode to use when opening the new compound file. For more information, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a> and the Remarks section below.


### -param reserved [in]

Reserved for future use; must be zero.


### -param ppstgOpen [out]

A pointer to the location of the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer on the new storage object.


## -returns



The <b>StgCreateDocfileOnILockBytes</b> function can also return any file system errors, or system errors wrapped in an <b>HRESULT</b>, or 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface error return values. For more information, see 
<a href="_com_error_handling_strategies">Error Handling Strategies</a> and 
<a href="_com_handling_unknown_errors">Handling Unknown Errors</a>.




## -remarks



The 
<b>StgCreateDocfileOnILockBytes</b> function creates a storage object on top of a byte array object using the COM-provided, compound-file implementation of the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface. 
<b>StgCreateDocfileOnILockBytes</b> can be used to store a document in an arbitrary data store, such as memory or a relational database. The byte array (indicated by the <i>pLkbyt</i> parameter, which points to the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface on the object) is used for the underlying storage in place of a disk file.

Except for specifying a programmer-provided byte-array object, 
<b>StgCreateDocfileOnILockBytes</b> is similar to the 
<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a> function. 

The newly created compound file is opened according to the access modes in the <i>grfMode</i> parameter, subject to the following restrictions: 

Sharing mode behavior and transactional isolation depend on the <a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> implementation supporting <a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">LockRegion</a> and <a href="https://msdn.microsoft.com/036ba242-8630-4013-860d-dd37919253be">UnlockRegion</a> with <a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCK_ONLYONCE</a> semantics.  Implementations can indicate to structured storage they support this functionality by setting the <b>LOCK_ONLYONCE</b> bit in the <b>grfLocksSupported</b> member of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>.  If an <b>ILockBytes</b> implementation does not support this functionality, sharing modes will not be enforced, and root-level transactional commits will not coordinate properly with other transactional instances opened on the same byte array.  Applications that use an <b>ILockBytes</b> implementation that does not support region locking, such as the <a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a> implementation, should avoid opening multiple concurrent instances on the same byte array.

<b>StgCreateDocfileOnILockBytes</b> does not support simple mode.  The <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM_SIMPLE</a> flag, if present, is ignored.

For conversion purposes, the file is considered to already exist. As a result, it is not useful to use the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM_FAILIFTHERE</a> value, because it causes an error to be returned. However, both STGM_CREATE and STGM_CONVERT remain useful.

The ability to build a compound file on top of a byte-array object is provided to support having the data (underneath an 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> and 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> tree structure) live in a nonpersistent space. Given this capability, there is nothing preventing a document that is stored in a file from using this facility. For example, a container might do this to minimize the impact on its file format caused by adopting COM. However, it is recommended that COM documents adopt the 
<b>IStorage</b> interface for their own outer-level storage. This has the following advantages:

<ul>
<li>The storage structure of the document is the same as its storage structure when it is an embedded object, reducing the number of cases the application needs to handle.</li>
<li>One can write tools to access the OLE embedded and linked objects within the document without special knowledge of the document's file format. An example of such a tool is a copy utility that copies all the documents included in a container containing linked objects. A copy utility like this needs access to the contained links to determine the extent of files to be copied.</li>
<li>The 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> implementation addresses the problem of how to commit the changes to the file. An application using the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface must handle these issues itself.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a>
 

 

