---
UID: NF:objidl.IStream.UnlockRegion
title: IStream::UnlockRegion (objidl.h)
description: The UnlockRegion method removes the access restriction on a range of bytes previously restricted with IStream::LockRegion.helpviewer_keywords: ["IStream interface [Structured Storage]","UnlockRegion method","IStream.UnlockRegion","IStream::UnlockRegion","UnlockRegion","UnlockRegion method [Structured Storage]","UnlockRegion method [Structured Storage]","IStream interface","_stg_istream_unlockregion","objidl/IStream::UnlockRegion","stg.istream_unlockregion"]
old-location: stg\istream_unlockregion.htm
tech.root: Stg
ms.assetid: e34c8d94-b24b-4041-b5dd-2a4ed74b01ec
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],UnlockRegion method, IStream.UnlockRegion, IStream::UnlockRegion, UnlockRegion, UnlockRegion method [Structured Storage], UnlockRegion method [Structured Storage],IStream interface, _stg_istream_unlockregion, objidl/IStream::UnlockRegion, stg.istream_unlockregion
f1_keywords:
- objidl/IStream.UnlockRegion
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IStream.UnlockRegion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStream::UnlockRegion


## -description


The <b>UnlockRegion</b> method removes the access restriction on a range of bytes previously restricted with 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-lockregion">IStream::LockRegion</a>.


## -parameters




### -param libOffset [in]

Specifies the byte offset for the beginning of the range.


### -param cb [in]

Specifies, in bytes, the length of the range to be restricted.


### -param dwLockType [in]

Specifies the access restrictions previously placed on the range.


## -returns



This method can return one of these values.




## -remarks



<b>IStream::UnlockRegion</b> unlocks a region previously locked with the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-lockregion">IStream::LockRegion</a> method. Locked regions must later be explicitly unlocked by calling <b>IStream::UnlockRegion</b> with exactly the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters. The region must be unlocked before the stream is released. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-lockregion">IStream::LockRegion</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a>
 

 

