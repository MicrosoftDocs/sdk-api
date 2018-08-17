---
UID: NF:coml2api.StgCreateDocfileOnILockBytes
title: StgCreateDocfileOnILockBytes function
author: windows-sdk-content
description: Creates and opens a new compound file storage object on top of a byte-array object provided by the caller.
old-location: stg\stgcreatedocfileonilockbytes.htm
old-project: stg
ms.assetid: 8af5098d-db04-4273-8f5f-6d1a1d9541de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: StgCreateDocfileOnILockBytes, StgCreateDocfileOnILockBytes function [Structured Storage], _stg_stgcreatedocfileonilockbytes, coml2api/StgCreateDocfileOnILockBytes, stg.stgcreatedocfileonilockbytes
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
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgCreateDocfileOnILockBytes
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# StgCreateDocfileOnILockBytes function


## -description


The <b>StgCreateDocfileOnILockBytes</b> function creates and opens a new compound file storage object on top of a byte-array object provided by the caller. The storage object supports the COM-provided, compound-file implementation for the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface.


## -parameters




### -param plkbyt [in]

A pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> interface on the underlying byte-array object on which to create a compound file.


### -param grfMode [in]

Specifies the access mode to use when opening the new compound file. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa380337(v=VS.85).aspx">STGM Constants</a> and the Remarks section below.


### -param reserved [in]

Reserved for future use; must be zero.


### -param ppstgOpen [out]

A pointer to the location of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> pointer on the new storage object.


## -returns



The <b>StgCreateDocfileOnILockBytes</b> function can also return any file system errors, or system errors wrapped in an <b>HRESULT</b>, or 
<a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> interface error return values. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/ms688560(v=VS.85).aspx">Error Handling Strategies</a> and 
<a href="https://msdn.microsoft.com/en-us/library/ms693442(v=VS.85).aspx">Handling Unknown Errors</a>.




## -remarks



The 
<b>StgCreateDocfileOnILockBytes</b> function creates a storage object on top of a byte array object using the COM-provided, compound-file implementation of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface. 
<b>StgCreateDocfileOnILockBytes</b> can be used to store a document in an arbitrary data store, such as memory or a relational database. The byte array (indicated by the <i>pLkbyt</i> parameter, which points to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> interface on the object) is used for the underlying storage in place of a disk file.

Except for specifying a programmer-provided byte-array object, 
<b>StgCreateDocfileOnILockBytes</b> is similar to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380323(v=VS.85).aspx">StgCreateDocfile</a> function. 

The newly created compound file is opened according to the access modes in the <i>grfMode</i> parameter, subject to the following restrictions: 

Sharing mode behavior and transactional isolation depend on the <a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> implementation supporting <a href="https://msdn.microsoft.com/en-us/library/Aa379242(v=VS.85).aspx">LockRegion</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa379250(v=VS.85).aspx">UnlockRegion</a> with <a href="https://msdn.microsoft.com/en-us/library/Aa380048(v=VS.85).aspx">LOCK_ONLYONCE</a> semantics.  Implementations can indicate to structured storage they support this functionality by setting the <b>LOCK_ONLYONCE</b> bit in the <b>grfLocksSupported</b> member of <a href="https://msdn.microsoft.com/en-us/library/Aa380319(v=VS.85).aspx">STATSTG</a>.  If an <b>ILockBytes</b> implementation does not support this functionality, sharing modes will not be enforced, and root-level transactional commits will not coordinate properly with other transactional instances opened on the same byte array.  Applications that use an <b>ILockBytes</b> implementation that does not support region locking, such as the <a href="https://msdn.microsoft.com/en-us/library/Aa378980(v=VS.85).aspx">CreateStreamOnHGlobal</a> implementation, should avoid opening multiple concurrent instances on the same byte array.

<b>StgCreateDocfileOnILockBytes</b> does not support simple mode.  The <a href="https://msdn.microsoft.com/en-us/library/Aa380337(v=VS.85).aspx">STGM_SIMPLE</a> flag, if present, is ignored.

For conversion purposes, the file is considered to already exist. As a result, it is not useful to use the <a href="https://msdn.microsoft.com/en-us/library/Aa380337(v=VS.85).aspx">STGM_FAILIFTHERE</a> value, because it causes an error to be returned. However, both STGM_CREATE and STGM_CONVERT remain useful.

The ability to build a compound file on top of a byte-array object is provided to support having the data (underneath an 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> and 
<a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a> tree structure) live in a nonpersistent space. Given this capability, there is nothing preventing a document that is stored in a file from using this facility. For example, a container might do this to minimize the impact on its file format caused by adopting COM. However, it is recommended that COM documents adopt the 
<b>IStorage</b> interface for their own outer-level storage. This has the following advantages:

<ul>
<li>The storage structure of the document is the same as its storage structure when it is an embedded object, reducing the number of cases the application needs to handle.</li>
<li>One can write tools to access the OLE embedded and linked objects within the document without special knowledge of the document's file format. An example of such a tool is a copy utility that copies all the documents included in a container containing linked objects. A copy utility like this needs access to the contained links to determine the extent of files to be copied.</li>
<li>The 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> implementation addresses the problem of how to commit the changes to the file. An application using the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379238(v=VS.85).aspx">ILockBytes</a> interface must handle these issues itself.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380323(v=VS.85).aspx">StgCreateDocfile</a>
 

 

