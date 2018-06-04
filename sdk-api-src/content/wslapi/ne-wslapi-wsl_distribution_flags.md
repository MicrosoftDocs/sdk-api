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

# WSL_DISTRIBUTION_FLAGS enumeration


## -description


The <b>WSL_DISTRIBUTION_FLAGS</b> enumeration specifies the behavior of a distribution in the Windows Subsystem for Linux (WSL).


## -enum-fields




### -field WSL_DISTRIBUTION_FLAGS_NONE

 No flags are being supplied.


### -field WSL_DISTRIBUTION_FLAGS_ENABLE_INTEROP

 Allow the distribution to interoperate with Windows processes (for example, the user can invoke "cmd.exe" or "notepad.exe" from within a WSL session).


### -field WSL_DISTRIBUTION_FLAGS_APPEND_NT_PATH

 Add the Windows %PATH% environment variable values to WSL sessions.


### -field WSL_DISTRIBUTION_FLAGS_ENABLE_DRIVE_MOUNTING

 Automatically mount Windows drives inside of WSL sessions (for example, "C:\" will be available under "/mnt/c").

