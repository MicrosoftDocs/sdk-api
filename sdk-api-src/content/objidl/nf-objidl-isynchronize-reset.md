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

# ISynchronize::Reset


## -description


Sets the synchronization object to the nonsignaled state.


## -parameters






## -returns



This method returns S_OK to indicate that the method completed successfully.




## -remarks



The <a href="https://msdn.microsoft.com/1abed0be-b4e3-41f4-af6c-e327ce934b59">ISynchronize::Wait</a> method implemented on a standard event object (CLSID_StdEvent) automatically calls <b>Reset</b> when the synchronization object has been signaled.

The implementation of <a href="https://msdn.microsoft.com/1abed0be-b4e3-41f4-af6c-e327ce934b59">ISynchronize::Wait</a> on the manual reset event object (CLSID_ManualResetEvent) does not automatically call <b>Reset</b>. A server object usually calls <b>Reset</b> from a method that clients call after they detect that the synchronization object was signaled.

In general, it is the server's responsibility to call <b>Reset</b>. If, however, the client needs to begin with the synchronization object in an unsignaled state, the client should call <b>Reset</b>.




## -see-also




<a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a>
 

 

