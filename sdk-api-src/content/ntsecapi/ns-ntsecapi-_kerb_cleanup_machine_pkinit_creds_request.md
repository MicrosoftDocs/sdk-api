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

# _KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST structure


## -description


The 	<b>KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST</b> structure cleans up the PKINIT device credentials from the computer.


## -struct-fields




### -field MessageType

The type of the message. You should set this to <b>KerbCleanupMachinePkinitCredsMessage</b>.


### -field LogonId

The logon session identifier. You should set this to SYSTEM LUID or NETWORKSERVICE LUID. TCB is required if this field is different from the caller's LUID.


## -remarks



You must clean up PKINIT device credentials for LOCAL_SYSTEM 	or NETWORK_SERVICE. When the PKINIT device credential is cleaned up, only the password credentials remain.



