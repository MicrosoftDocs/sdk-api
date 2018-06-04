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

# _RAS_PORT_CONDITION enumeration


## -description


The 
<b>RAS_PORT_CONDITION</b> enumerated type specifies information regarding the connection condition of a given RAS port.


## -enum-fields




### -field RAS_PORT_NON_OPERATIONAL

The port is not operational.


### -field RAS_PORT_DISCONNECTED

The port is disconnected.


### -field RAS_PORT_CALLING_BACK

The port is in the process of a call back.


### -field RAS_PORT_LISTENING

The port is listening for incoming calls.


### -field RAS_PORT_AUTHENTICATING

The port is authenticating a user.


### -field RAS_PORT_AUTHENTICATED

The port has authenticated a user.


### -field RAS_PORT_INITIALIZING

The port is initializing.


## -see-also




<a href="https://msdn.microsoft.com/6d044d35-5c50-4c30-89b4-8963d3b85673">RAS Administration Enumerated Types</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

