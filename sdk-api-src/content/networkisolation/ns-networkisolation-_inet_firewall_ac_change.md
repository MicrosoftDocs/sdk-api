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

# _INET_FIREWALL_AC_CHANGE structure


## -description


The <a href="https://msdn.microsoft.com/196f7150-185f-4234-a585-1a94d6dc24d7">INET_FIREWALL_AC_CHANGE</a> structure contains information about a change made to an app container.


## -struct-fields




### -field changeType

Type: <b><a href="https://msdn.microsoft.com/196f7150-185f-4234-a585-1a94d6dc24d7">INET_FIREWALL_AC_CHANGE_TYPE</a></b>

The type of change made.


### -field createType

Type: <b><a href="https://msdn.microsoft.com/01a1f735-889e-424e-860e-ca86f0abd126">INET_FIREWALL_AC_CREATION_TYPE</a></b>

The method by which the app container was created.


### -field appContainerSid

Type: <b>SID*</b>

The package identifier of the app container


### -field userSid

Type: <b>SID*</b>

The security identifier (SID) of the user to whom the app container belongs.


### -field displayName

Type: <b>LPWSTR</b>

Friendly name of the app container.


### -field u

 


### -field u.capabilities

 


### -field u.binaries

 




#### - binaries

Type: <b><a href="https://msdn.microsoft.com/5403303e-e65c-47cf-af84-3d748db8661b">INET_FIREWALL_AC_BINARIES</a></b>

Binary paths to the applications running in the changed app container.


#### - capabilities

Type: <b><a href="https://msdn.microsoft.com/37386225-0c64-49c0-a21c-cecd8bdb1f1f">INET_FIREWALL_AC_CAPABILITIES</a></b>

Information about the capabilities of the changed app container.


## -see-also




<a href="https://msdn.microsoft.com/5403303e-e65c-47cf-af84-3d748db8661b">INET_FIREWALL_AC_BINARIES</a>



<a href="https://msdn.microsoft.com/37386225-0c64-49c0-a21c-cecd8bdb1f1f">INET_FIREWALL_AC_CAPABILITIES</a>



<a href="https://msdn.microsoft.com/196f7150-185f-4234-a585-1a94d6dc24d7">INET_FIREWALL_AC_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/01a1f735-889e-424e-860e-ca86f0abd126">INET_FIREWALL_AC_CREATION_TYPE</a>
 

 

