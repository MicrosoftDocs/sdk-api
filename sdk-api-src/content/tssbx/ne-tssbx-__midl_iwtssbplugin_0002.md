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

# __MIDL_IWTSSBPlugin_0002 enumeration


## -description


Contains values that indicate the session mode of a Remote Desktop Session Host (RD Session Host) server.


## -enum-fields




### -field WTSSBX_MACHINE_SESSION_MODE_UNSPEC

The session mode of the server is unspecified.


### -field WTSSBX_MACHINE_SESSION_MODE_SINGLE

The server is in single session mode. It can only accept one session per user.


### -field WTSSBX_MACHINE_SESSION_MODE_MULTIPLE

The server is in multiple session mode. It can accept multiple sessions per user.

