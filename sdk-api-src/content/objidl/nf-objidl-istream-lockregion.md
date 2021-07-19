---
UID: NF:objidl.IStream.LockRegion
title: IStream::LockRegion (objidl.h)
description: The LockRegion method restricts access to a specified range of bytes in the stream.
helpviewer_keywords: ["IStream interface [Structured Storage]","LockRegion method","IStream.LockRegion","IStream::LockRegion","LockRegion","LockRegion method [Structured Storage]","LockRegion method [Structured Storage]","IStream interface","_stg_istream_lockregion","objidl/IStream::LockRegion","stg.istream_lockregion"]
old-location: stg\istream_lockregion.htm
tech.root: Stg
ms.assetid: f2606833-05ed-4bd0-a762-7b8172fb14c8
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],LockRegion method, IStream.LockRegion, IStream::LockRegion, LockRegion, LockRegion method [Structured Storage], LockRegion method [Structured Storage],IStream interface, _stg_istream_lockregion, objidl/IStream::LockRegion, stg.istream_lockregion
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
 - IStream::LockRegion
 - objidl/IStream::LockRegion
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
 - IStream.LockRegion
---

# IStream::LockRegion


## -description

The <b>LockRegion</b> method restricts access to a specified range of bytes in the stream. Supporting this functionality is optional since some file systems do not provide it.

## -parameters

### -param libOffset [in]

Integer that specifies the byte offset for the beginning of the range.

### -param cb [in]

Integer that specifies the length of the range, in bytes, to be restricted.

### -param dwLockType [in]

Specifies the restrictions being requested on accessing the range.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The specified range of bytes was locked.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream's data is currently unavailable. |
|STG_E_INVALIDFUNCTION | Locking is not supported at all or the specific type of lock requested is not supported.|
|STG_E_LOCKVIOLATION | Requested lock is supported, but cannot be granted because of an existing lock.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

The byte range of the stream can be extended.  Locking an extended range for the stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.

Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types. A given stream instance might support either of the first two types, or both. The lock type is specified by <i>dwLockType</i>, using a value from the 
<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a> enumeration.

Any region locked with <b>IStream::LockRegion</b> must later be explicitly unlocked by calling 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-unlockregion">IStream::UnlockRegion</a> with exactly the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters. The region must be unlocked before the stream is released. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Since the type of locking supported is optional and can vary in different implementations of 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>, you must provide code to deal with the STG_E_INVALIDFUNCTION error.

The <b>LockRegion</b> method has no effect in the compound file implementation, because the implementation does not support range locking.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Support for this method is optional for implementations of stream objects since it may not be supported by the underlying file system. The type of locking supported is also optional. The STG_E_INVALIDFUNCTION error is returned if the requested type of locking is not supported.

## -see-also

<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istream-unlockregion">IStream::UnlockRegion</a>



<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a>