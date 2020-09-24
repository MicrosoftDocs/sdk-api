---
UID: NF:wslapi.WslLaunchInteractive
title: WslLaunchInteractive function (wslapi.h)
description: Launches an interactive Windows Subsystem for Linux (WSL) process in the context of a particular distribution.
helpviewer_keywords: ["WslLaunchInteractive","WslLaunchInteractive function","wsl.wsllaunchinteractive","wslapi/WslLaunchInteractive"]
old-location: wsl\wsllaunchinteractive.htm
tech.root: wsl
ms.assetid: F9DF5B7A-D315-44B7-BB01-6440CCB4C64C
ms.date: 12/05/2018
ms.keywords: WslLaunchInteractive, WslLaunchInteractive function, wsl.wsllaunchinteractive, wslapi/WslLaunchInteractive
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
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WslLaunchInteractive
 - wslapi/WslLaunchInteractive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-wsl-api-l1-1-0.dll
api_name:
 - WslLaunchInteractive
---

# WslLaunchInteractive function


## -description

Launches an interactive Windows Subsystem for Linux (WSL) process in the context of a particular distribution.This differs from <a href="/previous-versions/windows/desktop/api/wslapi/nf-wslapi-wsllaunch">WslLaunch</a> in that the end user will be able to interact with the newly-created process.

## -parameters

### -param distributionName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").

### -param command [in, optional]

Command to execute. If no command is supplied, launches the default shell.

### -param useCurrentWorkingDirectory [in]

Governs whether or not the launched process should inherit the calling process's working directory. If FALSE, the process is started in the WSL default user's home directory ("~").

### -param exitCode [out]

Receives the exit code of the process after it exits.

## -returns

Returns S_OK on success, or a failing HRESULT otherwise.