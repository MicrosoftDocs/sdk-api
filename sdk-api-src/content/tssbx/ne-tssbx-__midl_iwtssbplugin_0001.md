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

# __MIDL_IWTSSBPlugin_0001 enumeration


## -description


Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server. The drain state indicates whether an RD Session Host server is accepting new connections. If the RD Session Host server is currently accepting new connections,  its drain state is off. If it is not accepting new connections, its drain state is on.


## -enum-fields




### -field WTSSBX_MACHINE_DRAIN_UNSPEC

The drain state of the server is unspecified.


### -field WTSSBX_MACHINE_DRAIN_OFF

The server is accepting new user sessions.


### -field WTSSBX_MACHINE_DRAIN_ON

The server is not accepting new user sessions.

