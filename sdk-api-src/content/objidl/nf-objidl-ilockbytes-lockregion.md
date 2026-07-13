---
UID: NF:objidl.ILockBytes.LockRegion
title: ILockBytes::LockRegion (objidl.h)
description: The LockRegion method restricts access to a specified range of bytes in the byte array.
helpviewer_keywords: ["ILockBytes interface [Structured Storage]","LockRegion method","ILockBytes.LockRegion","ILockBytes::LockRegion","LockRegion","LockRegion method [Structured Storage]","LockRegion method [Structured Storage]","ILockBytes interface","_stg_ilockbytes_lockregion","objidl/ILockBytes::LockRegion","stg.ilockbytes_lockregion"]
old-location: stg\ilockbytes_lockregion.htm
tech.root: Stg
ms.assetid: cea59e2a-99d8-472d-8e4f-2e2474789c20
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],LockRegion method, ILockBytes.LockRegion, ILockBytes::LockRegion, LockRegion, LockRegion method [Structured Storage], LockRegion method [Structured Storage],ILockBytes interface, _stg_ilockbytes_lockregion, objidl/ILockBytes::LockRegion, stg.ilockbytes_lockregion
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILockBytes::LockRegion
 - objidl/ILockBytes::LockRegion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes.LockRegion
---

# ILockBytes::LockRegion


## -description

The 
<b>LockRegion</b> method restricts access to a specified range of bytes in the byte array.

## -parameters

### -param libOffset [in]

Specifies the byte offset for the beginning of the range.

### -param cb [in]

Specifies, in bytes, the length of the range to be restricted.

### -param dwLockType [in]

Specifies the type of restrictions being requested on accessing the range. This parameter uses one of the values from the 
<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a> enumeration.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The specified range of bytes was locked.|
|STG_E_INVALIDFUNCTION | Locking is not supported at all or the specific type of lock requested is not supported.|
|STG_E_ACCESSDENIED | Access denied because the caller has insufficient permission, or another caller has the file open and locked.|
|STG_E_LOCKVIOLATION | Access denied because another caller has the file open and locked.|
|STG_E_INVALIDHANDLE | An underlying file has been prematurely closed, or the correct floppy disk has been replaced by an invalid one.|

## -remarks

<b>ILockBytes::LockRegion</b> restricts access to the specified range of bytes. Once a region is locked, attempts by others to gain access to the restricted range must fail with the STG_E_ACCESSDENIED error.

The byte range can extend past the current end of the byte array. Locking beyond the end of an array is useful as a method of communication between different instances of the byte array object without changing data that is actually part of the byte array. For example, an implementation of 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> for compound files could rely on locking past the current end of the array as a means of access control, using specific locked regions to indicate permissions currently granted.

The <i>dwLockType</i> parameter specifies one of three types of locking, using values from the 
<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a> enumeration. The types are as follows: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range. This third type of locking is usually an alias for one of the other two lock types, and permits an Implementer to add other behavior as well. A given byte array might support either of the first two types, or both.

To determine the lock types supported by a particular 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> implementation, you can examine the <b>grfLocksSupported</b> member of the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure returned by a call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-stat">ILockBytes::Stat</a>.

Any region locked with <b>ILockBytes::LockRegion</b> must later be explicitly unlocked by calling 
<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-unlockregion">ILockBytes::UnlockRegion</a> with exactly the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters. The region must be unlocked before the stream is released. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Since the type of locking supported is optional and can vary in different implementations of 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>, you must provide code to deal with the STG_E_INVALIDFUNCTION error.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Support for this method depends on how the storage object built on top of the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> implementation is used. If you know that only one storage object at any given time can be opened on the storage device that underlies the byte array, then your 
<b>ILockBytes</b> implementation does not need to support locking. However, if multiple simultaneous openings of a storage object are possible, then region locking is needed to coordinate them.

A 
<b>LockRegion</b> implementation can choose to support all, some, or none of the lock types. For unsupported lock types, the implementation should return STG_E_INVALIDFUNCTION.

## -see-also

<a href="/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-stat">ILockBytes::Stat</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-unlockregion">ILockBytes::UnlockRegion</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istream-lockregion">IStream::LockRegion</a>



<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a>