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

# WslLaunch function


## -description


Launches a Windows Subsystem for Linux (WSL) process in the context of a particular distribution.


## -parameters




### -param distributionName

TBD


### -param command [in, optional]

Command to execute. If no command is supplied, launches the default shell.


### -param useCurrentWorkingDirectory [in]

Governs whether or not the launched process should inherit the calling process's working directory. If FALSE, the process is started in the WSL default user's home directory ("~").


### -param stdIn

TBD


### -param stdOut

TBD


### -param stdErr

TBD


### -param process

TBD




#### - distroName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


#### - hStdErr [in]

Handle to use for <b>STDERR</b>.


#### - hStdIn [in]

Handle to use for <b>STDIN</b>.


#### - hStdOut [in]

Handle to use for <b>STDOUT</b>.


#### - phProcess [out]

Pointer to address to receive the process HANDLE associated with the newly-launched WSL process.


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.




## -remarks



Caller is responsible for calling <b>CloseHandle</b> on the value returned in <i>phProcess</i> on success.



