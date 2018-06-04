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

# _INET_FIREWALL_APP_CONTAINER structure


## -description


The <b>INET_FIREWALL_APP_CONTAINER</b> structure contains information about an specific app container.
<div class="code"></div>

## -struct-fields




### -field appContainerSid

Type: <b>SID*</b>

The package identifier of the app container


### -field userSid

Type: <b>SID*</b>

The security identifier (SID) of the user to whom the app container belongs.


### -field appContainerName

Type: <b>LPWSTR</b>

The app container's globally unique name.

 Also referred to as the  Package Family Name, for the app container of a Windows Store app.


### -field displayName

Type: <b>LPWSTR</b>

Friendly name of the app container


### -field description

Type: <b>LPWSTR</b>

A description of the app container (its use, the objective of the application that uses it, etc.)


### -field capabilities

Type: <b><a href="https://msdn.microsoft.com/37386225-0c64-49c0-a21c-cecd8bdb1f1f">INET_FIREWALL_AC_CAPABILITIES</a></b>

The capabilities of the app container.


### -field binaries

Type: <b><a href="https://msdn.microsoft.com/5403303e-e65c-47cf-af84-3d748db8661b">INET_FIREWALL_AC_BINARIES</a></b>

Binary paths to the applications running in the app container.


### -field workingDirectory

 


### -field packageFullName

 




## -see-also




<a href="https://msdn.microsoft.com/5403303e-e65c-47cf-af84-3d748db8661b">INET_FIREWALL_AC_BINARIES</a>



<a href="https://msdn.microsoft.com/37386225-0c64-49c0-a21c-cecd8bdb1f1f">INET_FIREWALL_AC_CAPABILITIES</a>
 

 

