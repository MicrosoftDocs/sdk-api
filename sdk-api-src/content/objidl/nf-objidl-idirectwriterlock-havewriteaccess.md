---
UID: NF:objidl.IDirectWriterLock.HaveWriteAccess
title: IDirectWriterLock::HaveWriteAccess (objidl.h)
description: The HaveWriteAccess method indicates whether the write lock has been taken.
helpviewer_keywords: ["HaveWriteAccess","HaveWriteAccess method [Structured Storage]","HaveWriteAccess method [Structured Storage]","IDirectWriterLock interface","IDirectWriterLock interface [Structured Storage]","HaveWriteAccess method","IDirectWriterLock.HaveWriteAccess","IDirectWriterLock::HaveWriteAccess","_stg_idirectwriterlock_havewriteaccess","objidl/IDirectWriterLock::HaveWriteAccess","stg.idirectwriterlock_havewriteaccess"]
old-location: stg\idirectwriterlock_havewriteaccess.htm
tech.root: Stg
ms.assetid: 8366b6b5-73c3-4b05-be68-c24ecd2eab96
ms.date: 12/05/2018
ms.keywords: HaveWriteAccess, HaveWriteAccess method [Structured Storage], HaveWriteAccess method [Structured Storage],IDirectWriterLock interface, IDirectWriterLock interface [Structured Storage],HaveWriteAccess method, IDirectWriterLock.HaveWriteAccess, IDirectWriterLock::HaveWriteAccess, _stg_idirectwriterlock_havewriteaccess, objidl/IDirectWriterLock::HaveWriteAccess, stg.idirectwriterlock_havewriteaccess
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
 - IDirectWriterLock::HaveWriteAccess
 - objidl/IDirectWriterLock::HaveWriteAccess
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
 - IDirectWriterLock.HaveWriteAccess
---

# IDirectWriterLock::HaveWriteAccess


## -description

The <b>HaveWriteAccess</b> method indicates whether the write lock has been taken.



## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The storage object is currently locked for write access.|
|S_FALSE | The storage object is not currently locked for write access.|

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-releasewriteaccess">IDirectWriterLock::ReleaseWriteAccess</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-waitforwriteaccess">IDirectWriterLock::WaitForWriteAccess</a>
