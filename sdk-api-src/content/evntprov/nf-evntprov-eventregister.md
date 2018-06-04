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

# EventRegister function


## -description


Registers the provider.


## -parameters




### -param ProviderId [in]

GUID that uniquely identifies the provider.


### -param EnableCallback [in, optional]

Callback that ETW  calls to notify you when a session enables or disables your provider. Can be 
      <b>NULL</b>.


### -param CallbackContext [in, optional]

Provider-defined context data to pass to the callback when the provider is enabled or disabled. Can be 
      <b>NULL</b>.


### -param RegHandle [out]

Registration handle. The handle is used by most provider function calls. Before your provider exits, you 
      must pass this handle to <a href="https://msdn.microsoft.com/fdcccf6f-2f31-4356-a4ee-3b6229c01b75">EventUnregister</a> to 
      free the handle.


## -returns



Returns ERROR_SUCCESS if successful.




## -remarks



Use this function to register your provider if you call 
    <a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a> to write your events.

A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that 
     your process registers to one or two. This limit includes those registered using this function and the 
     <a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function.

<b>Prior to Windows Vista:  </b>There is no limit to the number of providers that a process can register. 




## -see-also




<a href="https://msdn.microsoft.com/f339323e-9da9-495f-aac5-f44969a018eb">EnableCallback</a>



<a href="https://msdn.microsoft.com/fdcccf6f-2f31-4356-a4ee-3b6229c01b75">EventUnregister</a>
 

 

