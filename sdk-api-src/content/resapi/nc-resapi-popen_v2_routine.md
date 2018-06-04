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

# POPEN_V2_ROUTINE callback function


## -description


Opens a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
    <b>POPEN_V2_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceName [in]

The name of the resource to open.


### -param ResourceKey [in]

The <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key for the 
       cluster that includes the resource represented by 
       <i>ResourceName</i>.


### -param ResourceHandle [in]

The resource handle to pass to the <a href="https://msdn.microsoft.com/3733F912-9D43-489B-91D8-7128D0F5D1A4">SetResourceStatusEx</a> 
       callback function.


### -param OpenFlags [in]

One of the following flags:



#### 0x0

TBD



#### CLUS_RESDLL_OPEN_RECOVER_MONITOR_STATE (0x00000001)

TBD


## -returns



If the operation was successful, returns a resource 
       identifier (<b>RESID</b>).

If the operation was not successful, returns 
       <b>NULL</b>. Call  <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to 
       specify that an error has occurred.




## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

