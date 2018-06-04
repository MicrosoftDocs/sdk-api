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

# tagWPCFLAG_LOGOFF_TYPE enumeration


## -description


Indicates information about the type of logoff method used.


## -enum-fields




### -field WPCFLAG_LOGOFF_TYPE_LOGOUT

The user logged off by logging off the computer.


### -field WPCFLAG_LOGOFF_TYPE_RESTART

The user logged off by restarting the computer.


### -field WPCFLAG_LOGOFF_TYPE_SHUTDOWN

The user logged off by shutting down the computer.


### -field WPCFLAG_LOGOFF_TYPE_FUS

The user logged off by using fast user switching.


### -field WPCFLAG_LOGOFF_TYPE_FORCEDFUS

The user was forced to log off by fast user switching.

