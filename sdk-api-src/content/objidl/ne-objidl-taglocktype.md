---
UID: NE:objidl.tagLOCKTYPE
title: tagLOCKTYPE
author: windows-sdk-content
description: The LOCKTYPE enumeration values indicate the type of locking requested for the specified range of bytes. The values are used in the ILockBytes::LockRegion and IStream::LockRegion methods.
old-location: stg\locktype.htm
tech.root: Stg
ms.assetid: 5d84fb08-aa4f-4918-a0de-550b02cb5287
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LOCKTYPE, LOCKTYPE enumeration [Structured Storage], LOCK_EXCLUSIVE, LOCK_ONLYONCE, LOCK_WRITE, _stg_locktype, objidl/LOCKTYPE, objidl/LOCK_EXCLUSIVE, objidl/LOCK_ONLYONCE, objidl/LOCK_WRITE, stg.locktype, tagLOCKTYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - LOCKTYPE
product: Windows
targetos: Windows
req.typenames: LOCKTYPE
req.redist: 
---

# tagLOCKTYPE enumeration


## -description


The 
<b>LOCKTYPE</b> enumeration values indicate the type of locking requested for the specified range of bytes. The values are used in the 
<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a> and 
<a href="https://msdn.microsoft.com/f2606833-05ed-4bd0-a762-7b8172fb14c8">IStream::LockRegion</a> methods.


## -enum-fields




### -field LOCK_WRITE

If this lock is granted, the specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.


### -field LOCK_EXCLUSIVE

If this lock is granted, writing to the specified range of bytes is prohibited except by the owner that was granted this lock.


### -field LOCK_ONLYONCE

If this lock is granted, no other <b>LOCK_ONLYONCE</b> lock can be obtained on the range. Usually this lock type is an alias for some other lock type. Thus, specific implementations can have additional behavior associated with this lock type.

