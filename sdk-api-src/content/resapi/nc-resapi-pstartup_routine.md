---
UID: NC:resapi.PSTARTUP_ROUTINE
title: PSTARTUP_ROUTINE
author: windows-driver-content
description: Loads a resource DLL, returning a structure containing a function table and a version number.
old-location: mscs\startup.htm
old-project: MsCS
ms.assetid: b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PSTARTUP_ROUTINE, PSTARTUP_ROUTINE callback function [Failover Cluster], Startup, Startup callback, Startup callback function [Failover Cluster], _wolf_startup, mscs.startup, resapi/PSTARTUP_ROUTINE, resapi/Startup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	Startup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSTARTUP_ROUTINE callback function


## -description


Loads a <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>, returning a structure 
    containing a function table and a version number. The <b>PSTARTUP_ROUTINE</b> 
    type defines a pointer to this function.


## -parameters




### -param ResourceType [in]

Type of resource being started.


### -param MinVersionSupported [in]

Minimum version of the <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> supported by the 
       <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>.


### -param MaxVersionSupported [in]

Maximum version of the Resource API supported by the Cluster service.


### -param SetResourceStatus [in]

Pointer to a callback function that the resource DLL should call to update its status after returning 
       <b>ERROR_IO_PENDING</b> from <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a> or 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>. For more information see 
       <a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a>.


### -param LogEvent [in]

Pointer to a callback function that the resource DLL should call to report events for the 
       <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. For more information see 
       <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a>.


### -param *FunctionTable [out]

Pointer to a <a href="https://msdn.microsoft.com/fa27076f-393c-415a-9301-91cfe770fb3c">CLRES_FUNCTION_TABLE</a> structure 
       that describes the Resource API version and the specific names for the entry points.


## -returns



If the operation was not successful, <i>Startup</i> should 
       return one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



The <i>Startup</i> entry-point function returns a function table 
     that describes both the supported interface version of the Resource API and the entry points for all other 
     functions required by the supported version of the Resource API.

At present, only Resource API version 1.0 is supported.

If your resource supports more than one version of the Resource API, return a function table for the latest 
     version. The version number should be less than or equal to the <i>MaxVersionSupported</i> 
     parameter. If the version of the function table pointed to by the <i>FunctionTable</i> 
     parameter is not within range, your resource cannot be loaded successfully.

For more information see <a href="https://msdn.microsoft.com/022f1e0b-fbd0-480c-9889-879e5d7458a3">Implementing Startup</a>.


#### Examples

See <a href="https://msdn.microsoft.com/022f1e0b-fbd0-480c-9889-879e5d7458a3">Implementing Startup</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

