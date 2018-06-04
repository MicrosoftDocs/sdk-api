---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

