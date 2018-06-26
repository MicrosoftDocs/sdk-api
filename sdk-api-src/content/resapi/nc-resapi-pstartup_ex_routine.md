---
UID: NC:resapi.PSTARTUP_EX_ROUTINE
title: PSTARTUP_EX_ROUTINE
author: windows-sdk-content
description: Loads a resource DLL, returning a structure that contains a function table and a version number.
old-location: mscs\startupex.htm
old-project: MsCS
ms.assetid: 7C669EDC-B7A1-4623-91A9-5D8C5949B50A
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PSTARTUP_EX_ROUTINE, PSTARTUP_EX_ROUTINE callback function [Failover Cluster], StartupEx, StartupEx callback, StartupEx callback function [Failover Cluster], mscs.startupex, resapi/PSTARTUP_EX_ROUTINE, resapi/StartupEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - StartupEx callback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

