---
UID: NF:wsman.WSManCloseCommand
title: WSManCloseCommand function
author: windows-sdk-content
description: Deletes a command and frees the resources that are associated with it.
old-location: winrm\wsmanclosecommand.htm
tech.root: winrm
ms.assetid: 41ef2a6d-af1a-4a51-b01d-262380f01187
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSManCloseCommand, WSManCloseCommand function [Windows Remote Management], winrm.wsmanclosecommand, wsman/WSManCloseCommand
ms.topic: function
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManCloseCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
---

# WSManCloseCommand function


## -description


Deletes a command and frees the resources that are associated with it.


## -parameters




### -param commandHandle [in, out, optional]

Specifies the command handle to be closed. This handle is returned by a <a href="https://msdn.microsoft.com/8f5c89f8-418c-4a4d-9a52-0fc01ec636b2">WSManRunShellCommand</a> call.


### -param flags

Reserved for future use.
Must be set to zero.


### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a> structure for more information.  This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



