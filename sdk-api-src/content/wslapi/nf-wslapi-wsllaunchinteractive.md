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

# WslLaunchInteractive function


## -description


Launches an interactive Windows Subsystem for Linux (WSL) process in the context of a particular distribution.This differs from <a href="https://msdn.microsoft.com/0C88BCF8-9FFC-4D7C-9A7C-F56F9A4FD7FC">WslLaunch</a> in that the end user will be able to interact with the newly-created process.


## -parameters




### -param distributionName

TBD


### -param command [in, optional]

Command to execute. If no command is supplied, launches the default shell.


### -param useCurrentWorkingDirectory [in]

Governs whether or not the launched process should inherit the calling process's working directory. If FALSE, the process is started in the WSL default user's home directory ("~").


### -param exitCode

TBD




#### - *pExitCode [out]

Receives the exit code of the process after it exits.


#### - distroName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.



