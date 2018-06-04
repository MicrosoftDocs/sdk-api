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

# _TSSESSION_STATE enumeration


## -description


Indicates the state of a session.


## -enum-fields




### -field STATE_INVALID

The session state is not valid.


### -field STATE_ACTIVE

The user is logged on to WinStation.


### -field STATE_CONNECTED

WinStation is connected to the client (session reconnected).


### -field STATE_CONNECTQUERY

In the process of connecting to the client (session reconnect pending).


### -field STATE_SHADOW

Shadowing another WinStation.


### -field STATE_DISCONNECTED

WinStation is active but the client is disconnected.


### -field STATE_IDLE

Waiting for the client to connect.


### -field STATE_LISTEN

WinStation is listening for a connection.


### -field STATE_RESET

WinStation is being reset (session logged off).


### -field STATE_DOWN

WinStation is down due to error.


### -field STATE_INIT

WinStation is initializing.


### -field STATE_MAX




## -see-also




<a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a>
 

 

