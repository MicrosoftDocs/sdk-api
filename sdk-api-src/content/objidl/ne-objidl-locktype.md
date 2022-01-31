---
UID: NE:objidl.tagLOCKTYPE
title: LOCKTYPE (objidl.h)
description: The LOCKTYPE enumeration values indicate the type of locking requested for the specified range of bytes. The values are used in the ILockBytes::LockRegion and IStream::LockRegion methods.
helpviewer_keywords: ["LOCKTYPE","LOCKTYPE enumeration [Structured Storage]","LOCK_EXCLUSIVE","LOCK_ONLYONCE","LOCK_WRITE","_stg_locktype","objidl/LOCKTYPE","objidl/LOCK_EXCLUSIVE","objidl/LOCK_ONLYONCE","objidl/LOCK_WRITE","stg.locktype"]
old-location: stg\locktype.htm
tech.root: Stg
ms.assetid: 5d84fb08-aa4f-4918-a0de-550b02cb5287
ms.date: 12/05/2018
ms.keywords: LOCKTYPE, LOCKTYPE enumeration [Structured Storage], LOCK_EXCLUSIVE, LOCK_ONLYONCE, LOCK_WRITE, _stg_locktype, objidl/LOCKTYPE, objidl/LOCK_EXCLUSIVE, objidl/LOCK_ONLYONCE, objidl/LOCK_WRITE, stg.locktype
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LOCKTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLOCKTYPE
 - objidl/tagLOCKTYPE
 - LOCKTYPE
 - objidl/LOCKTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - LOCKTYPE
---

# LOCKTYPE enumeration


## -description

The 
<b>LOCKTYPE</b> enumeration values indicate the type of locking requested for the specified range of bytes. The values are used in the 
<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-lockregion">ILockBytes::LockRegion</a> and 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-lockregion">IStream::LockRegion</a> methods.

## -enum-fields

### -field LOCK_WRITE:1

If this lock is granted, the specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.

### -field LOCK_EXCLUSIVE:2

If this lock is granted, writing to the specified range of bytes is prohibited except by the owner that was granted this lock.

### -field LOCK_ONLYONCE:4

If this lock is granted, no other <b>LOCK_ONLYONCE</b> lock can be obtained on the range. Usually this lock type is an alias for some other lock type. Thus, specific implementations can have additional behavior associated with this lock type.
