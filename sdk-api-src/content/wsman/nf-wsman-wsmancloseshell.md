---
UID: NF:wsman.WSManCloseShell
title: WSManCloseShell function
author: windows-sdk-content
description: Deletes a shell object and frees the resources associated with the shell.
old-location: winrm\wsmancloseshell.htm
tech.root: WinRM
ms.assetid: 1da452ef-5842-4d8d-941b-09fa57393ebb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WSManCloseShell, WSManCloseShell function [Windows Remote Management], winrm.wsmancloseshell, wsman/WSManCloseShell
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSManCloseShell
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
- apiref
: 
- 
: 
- WSManCloseShell
: 
---

# WSManCloseShell function


## -description


Deletes a shell object and frees the resources associated with the shell.


## -parameters




### -param shellHandle [in, out, optional]

Specifies the shell handle to close. This handle is returned by a <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.


### -param flags

Reserved for future use. Must be set to zero.


### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a> structure for more information.  This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



