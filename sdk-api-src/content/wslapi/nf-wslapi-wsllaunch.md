---
UID: NF:wslapi.WslLaunch
title: WslLaunch function
author: windows-sdk-content
description: Launches a Windows Subsystem for Linux (WSL) process in the context of a particular distribution.
old-location: wsl\wsllaunch.htm
old-project: wsl
ms.assetid: 0C88BCF8-9FFC-4D7C-9A7C-F56F9A4FD7FC
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WslLaunch, WslLaunch function, wsl.wsllaunch, wslapi/WslLaunch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wslapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-wsl-api-l1-1-0.dll
api_name:
 - WslLaunch
product: Windows
targetos: Windows
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WslLaunch function


## -description


Launches a Windows Subsystem for Linux (WSL) process in the context of a particular distribution.


## -parameters




### -param distributionName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


### -param command [in, optional]

Command to execute. If no command is supplied, launches the default shell.


### -param useCurrentWorkingDirectory [in]

Governs whether or not the launched process should inherit the calling process's working directory. If FALSE, the process is started in the WSL default user's home directory ("~").


### -param stdIn [in]

Handle to use for <b>STDIN</b>.


### -param stdOut [in]

Handle to use for <b>STDOUT</b>.


### -param stdErr [in]

Handle to use for <b>STDERR</b>.


### -param process [out]

Pointer to address to receive the process HANDLE associated with the newly-launched WSL process.


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.




## -remarks



Caller is responsible for calling <b>CloseHandle</b> on the value returned in <i>phProcess</i> on success.



