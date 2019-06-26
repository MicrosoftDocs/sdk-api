---
UID: NE:wslapi.__unnamed_enum_0
title: WSL_DISTRIBUTION_FLAGS (wslapi.h)
author: windows-sdk-content
description: The WSL_DISTRIBUTION_FLAGS enumeration specifies the behavior of a distribution in the Windows Subsystem for Linux (WSL).
old-location: wsl\wsl_distribution_flags.htm
tech.root: wsl
ms.assetid: C0E67521-2C18-4464-B0BC-BBBC4C1FCAF0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSL_DISTRIBUTION_FLAGS, WSL_DISTRIBUTION_FLAGS enumeration, WSL_DISTRIBUTION_FLAGS_APPEND_NT_PATH, WSL_DISTRIBUTION_FLAGS_ENABLE_DRIVE_MOUNTING, WSL_DISTRIBUTION_FLAGS_ENABLE_INTEROP, WSL_DISTRIBUTION_FLAGS_NONE, wsl.wsl_distribution_flags, wslapi/WSL_DISTRIBUTION_FLAGS, wslapi/WSL_DISTRIBUTION_FLAGS_APPEND_NT_PATH, wslapi/WSL_DISTRIBUTION_FLAGS_ENABLE_DRIVE_MOUNTING, wslapi/WSL_DISTRIBUTION_FLAGS_ENABLE_INTEROP, wslapi/WSL_DISTRIBUTION_FLAGS_NONE
ms.topic: enum
f1_keywords: 
 - "wslapi/WSL_DISTRIBUTION_FLAGS"
req.header: wslapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wslapi.h
api_name:
 - WSL_DISTRIBUTION_FLAGS
product: Windows
targetos: Windows
req.typenames: WSL_DISTRIBUTION_FLAGS
req.redist: 
ms.custom: 19H1
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

