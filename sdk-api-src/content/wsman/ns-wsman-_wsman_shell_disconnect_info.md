---
UID: NS:wsman._WSMAN_SHELL_DISCONNECT_INFO
title: "_WSMAN_SHELL_DISCONNECT_INFO"
author: windows-sdk-content
description: Specifies the maximum duration, in milliseconds, the shell will stay open after the client has disconnected.
old-location: winrm\wsman_shell_disconnect_info.htm
old-project: WinRM
ms.assetid: CFC855E8-25C9-45A1-8D59-55AD5D4A75F3
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PWSMAN_SHELL_DISCONNECT_INFO, PWSMAN_SHELL_DISCONNECT_INFO structure pointer [Windows Remote Management], WSMAN_SHELL_DISCONNECT_INFO, WSMAN_SHELL_DISCONNECT_INFO structure [Windows Remote Management], _WSMAN_SHELL_DISCONNECT_INFO, winrm.wsman_shell_disconnect_info, wsman/PWSMAN_SHELL_DISCONNECT_INFO, wsman/WSMAN_SHELL_DISCONNECT_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WSMAN_SHELL_DISCONNECT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_DISCONNECT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_SHELL_DISCONNECT_INFO structure


## -description


Specifies the maximum duration, in milliseconds, the shell will stay open after the client has disconnected.


## -struct-fields




### -field idleTimeoutMs

Specifies the maximum time  in milliseconds that the shell will stay open after the client has disconnected. When this maximum duration has been exceeded, the shell will be deleted. Specifying this value overrides the initial idle timeout value that is set as part of the <a href="https://msdn.microsoft.com/a9e004de-b157-4ad3-a463-a42ccb56f1ba">WSMAN_SHELL_STARTUP_INFO</a> structure in the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> method.


## -remarks



When the maximum duration is exceeded, the shell is automatically deleted. This value overrides the initial idle timeout that is set as part of <a href="https://msdn.microsoft.com/a9e004de-b157-4ad3-a463-a42ccb56f1ba">WSMAN_SHELL_STARTUP_INFO</a> structure in <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a>.



