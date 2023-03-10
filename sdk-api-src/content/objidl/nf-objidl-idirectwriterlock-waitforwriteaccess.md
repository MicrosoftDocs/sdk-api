---
UID: NF:objidl.IDirectWriterLock.WaitForWriteAccess
title: IDirectWriterLock::WaitForWriteAccess (objidl.h)
description: The WaitForWriteAccess method obtains exclusive write access to a storage object.
helpviewer_keywords: ["IDirectWriterLock interface [Structured Storage]","WaitForWriteAccess method","IDirectWriterLock.WaitForWriteAccess","IDirectWriterLock::WaitForWriteAccess","WaitForWriteAccess","WaitForWriteAccess method [Structured Storage]","WaitForWriteAccess method [Structured Storage]","IDirectWriterLock interface","_stg_idirectwriterlock_waitforwriteaccess","objidl/IDirectWriterLock::WaitForWriteAccess","stg.idirectwriterlock_waitforwriteaccess"]
old-location: stg\idirectwriterlock_waitforwriteaccess.htm
tech.root: Stg
ms.assetid: e4505bed-325b-494e-93bd-7bf23b3a1215
ms.date: 12/05/2018
ms.keywords: IDirectWriterLock interface [Structured Storage],WaitForWriteAccess method, IDirectWriterLock.WaitForWriteAccess, IDirectWriterLock::WaitForWriteAccess, WaitForWriteAccess, WaitForWriteAccess method [Structured Storage], WaitForWriteAccess method [Structured Storage],IDirectWriterLock interface, _stg_idirectwriterlock_waitforwriteaccess, objidl/IDirectWriterLock::WaitForWriteAccess, stg.idirectwriterlock_waitforwriteaccess
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
 - IDirectWriterLock::WaitForWriteAccess
 - objidl/IDirectWriterLock::WaitForWriteAccess
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
 - IDirectWriterLock.WaitForWriteAccess
---

# IDirectWriterLock::WaitForWriteAccess


## -description

The <b>WaitForWriteAccess</b> method obtains exclusive write access to a storage object.

## -parameters

### -param dwTimeout [in]

Specifies the time in milliseconds that this method blocks while waiting to obtain exclusive write access to the storage object. If <i>dwTimeout</i> is zero, the method does not block waiting for exclusive access for writing. The INFINITE time-out defined in the Platform SDK is allowed for <i>dwTimeout</i>.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The caller has successfully obtained exclusive write access to the storage.|
|S_FALSE | This method was called again without an intervening call to IDirectWriterLock::ReleaseWriteAccess.|
|STG_E_INUSE | The specified time-out expired without obtaining exclusive write access.|

## -remarks

When a storage is opened in direct mode (STGM_DIRECT) with the STGM_READWRITE|STGM_SHARE_DENY_WRITE, you can call this method to obtain exclusive write access to the storage.

This method returns immediately if no readers have the storage open. If the storage is still open for reading, this method blocks for the specified <i>dwTimeout</i> or until the current readers close the storage.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-havewriteaccess">IDirectWriterLock::HaveWriteAccess</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-releasewriteaccess">IDirectWriterLock::ReleaseWriteAccess</a>