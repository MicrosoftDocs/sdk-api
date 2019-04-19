---
UID: NF:objidl.IDirectWriterLock.ReleaseWriteAccess
title: IDirectWriterLock::ReleaseWriteAccess (objidl.h)
author: windows-sdk-content
description: The ReleaseWriteAccess method releases the write lock previously obtained.
old-location: stg\idirectwriterlock_releasewriteaccess.htm
tech.root: Stg
ms.assetid: 849eeb79-60fd-4345-9e04-2ed7a7ede5ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectWriterLock interface [Structured Storage],ReleaseWriteAccess method, IDirectWriterLock.ReleaseWriteAccess, IDirectWriterLock::ReleaseWriteAccess, ReleaseWriteAccess, ReleaseWriteAccess method [Structured Storage], ReleaseWriteAccess method [Structured Storage],IDirectWriterLock interface, _stg_idirectwriterlock_releasewriteaccess, objidl/IDirectWriterLock::ReleaseWriteAccess, stg.idirectwriterlock_releasewriteaccess
ms.topic: method
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
 - IDirectWriterLock.ReleaseWriteAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectWriterLock::ReleaseWriteAccess


## -description


The <b>ReleaseWriteAccess</b> method releases the write lock previously obtained.


## -parameters






## -returns



This method can return one of these values.




## -remarks



The writer calls this method to release exclusive access to the storage object previously taken by calling <a href="https://msdn.microsoft.com/e4505bed-325b-494e-93bd-7bf23b3a1215">IDirectWriterLock::WaitForWriteAccess</a>.

After the writer calls this method, it is safe to allow readers to reopen the storage again until the next call to <a href="https://msdn.microsoft.com/e4505bed-325b-494e-93bd-7bf23b3a1215">IDirectWriterLock::WaitForWriteAccess</a>.




## -see-also




<a href="https://msdn.microsoft.com/8366b6b5-73c3-4b05-be68-c24ecd2eab96">IDirectWriterLock::HaveWriteAccess</a>



<a href="https://msdn.microsoft.com/e4505bed-325b-494e-93bd-7bf23b3a1215">IDirectWriterLock::WaitForWriteAccess</a>
 

 

