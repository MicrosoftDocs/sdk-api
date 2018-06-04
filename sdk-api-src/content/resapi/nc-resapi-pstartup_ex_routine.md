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

# PSTARTUP_EX_ROUTINE callback function


## -description


Loads a <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>, returning a structure 
    that contains a function table and a version number. The <b>PSTARTUP_EX_ROUTINE</b> 
    type defines a pointer to this function.


## -parameters




### -param ResourceType [in]

The type of resource to start.


### -param MinVersionSupported [in]

The minimum version of the <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> supported by the 
       <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>.


### -param MaxVersionSupported [in]

The maximum version of the Resource API supported by the Cluster service.


### -param MonitorCallbackFunctions [in]

TBD


### -param *ResourceDllInterfaceFunctions [out]

TBD


## -returns





Returns DWORD that ...






## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

