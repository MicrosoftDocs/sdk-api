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

# IRDPSRAPIApplicationFilter interface


## -description


Manages the shared desktop area at the window and process level. Applications can use the enumerators to display lists of objects in the session that can be shared.

Applications can obtain access to this object using <a href="https://msdn.microsoft.com/4a346305-972c-40c4-882e-905745edf6e9">IRDPSRAPISharingSession::ApplicationFilter</a>.

The list of sharable objects is exposed as a two-level tree. Each window has an application object as a parent. Each window object has its own sharing state that can be overridden by the sharing state of its parent. Each application object has its own sharing state that can be overridden by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property of the application filter. Therefore, if an application filter is enabled and the application is shared, its windows are shared regardless of their sharing state. If the application filter is enabled but the application is not shared, its windows are shared depending on their sharing state.

If a shared application creates a new window that is sharable, it will be shared because the parent application is shared.


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/9a934718-1eea-4406-a1da-b7d493f6667e">IRDPSRAPIApplication</a>



<a href="https://msdn.microsoft.com/275bb93c-dc93-4884-82a9-e87f5c3ab475">IRDPSRAPIApplicationList</a>
 

 

