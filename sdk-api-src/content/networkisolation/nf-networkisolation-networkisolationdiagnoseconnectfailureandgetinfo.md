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

# NetworkIsolationDiagnoseConnectFailureAndGetInfo function


## -description


The <b>NetworkIsolationDiagnoseConnectFailureAndGetInfo</b> function gets information about a network isolation connection failure due to a missing capability. This function can be used to identify the capabilities required to connect to a server.


## -parameters




### -param wszServerName [in]

Type: <b>LPCWSTR</b>

Name (or IP address literal string) of the server to which a connection was attempted.


### -param netIsoError [out]

Type: <b><a href="https://msdn.microsoft.com/0daa9d07-8a65-4254-b197-a37e6e04ce32">NETISO_ERROR_TYPE</a>*</b>

The error that has occurred, indicating which network capability was missing and thus caused the failure.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 




## -see-also




<a href="https://msdn.microsoft.com/0daa9d07-8a65-4254-b197-a37e6e04ce32">NETISO_ERROR_TYPE</a>
 

 

