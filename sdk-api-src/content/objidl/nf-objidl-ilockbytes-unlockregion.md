---
UID: NF:objidl.ILockBytes.UnlockRegion
title: ILockBytes::UnlockRegion (objidl.h)
description: The UnlockRegion method removes the access restriction on a previously locked range of bytes.
helpviewer_keywords: ["ILockBytes interface [Structured Storage]","UnlockRegion method","ILockBytes.UnlockRegion","ILockBytes::UnlockRegion","UnlockRegion","UnlockRegion method [Structured Storage]","UnlockRegion method [Structured Storage]","ILockBytes interface","_stg_ilockbytes_unlockregion","objidl/ILockBytes::UnlockRegion","stg.ilockbytes_unlockregion"]
old-location: stg\ilockbytes_unlockregion.htm
tech.root: Stg
ms.assetid: 036ba242-8630-4013-860d-dd37919253be
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],UnlockRegion method, ILockBytes.UnlockRegion, ILockBytes::UnlockRegion, UnlockRegion, UnlockRegion method [Structured Storage], UnlockRegion method [Structured Storage],ILockBytes interface, _stg_ilockbytes_unlockregion, objidl/ILockBytes::UnlockRegion, stg.ilockbytes_unlockregion
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
 - ILockBytes::UnlockRegion
 - objidl/ILockBytes::UnlockRegion
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
 - ILockBytes.UnlockRegion
---

# ILockBytes::UnlockRegion


## -description

The <b>UnlockRegion</b> method removes the access restriction on a previously locked range of bytes.

## -parameters

### -param libOffset [in]

Specifies the byte offset for the beginning of the range.

### -param cb [in]

Specifies, in bytes, the length of the range that is restricted.

### -param dwLockType [in]

Specifies the type of access restrictions previously placed on the range. This parameter uses a value from the 
<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a> enumeration.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The byte range was unlocked.|
|STG_E_INVALIDFUNCTION | Locking is not supported at all or the specific type of lock requested is not supported.|
|STG_E_LOCKVIOLATION | The requested unlock cannot be granted.|

## -remarks

<b>ILockBytes::UnlockRegion</b> unlocks a region previously locked with a call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-lockregion">ILockBytes::LockRegion</a>. Each region locked must be explicitly unlocked, using the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters as in the matching calls to <b>ILockBytes::LockRegion</b>. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.

## -see-also

<a href="/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-lockregion">ILockBytes::LockRegion</a>



<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a>