---
UID: NF:wsman.WSManSignalShell
title: WSManSignalShell function (wsman.h)
description: Sends a control code to an existing command or to the shell itself.
helpviewer_keywords: ["WSMAN_SIGNAL_SHELL_CODE_CTRL_BREAK","WSMAN_SIGNAL_SHELL_CODE_CTRL_C","WSMAN_SIGNAL_SHELL_CODE_TERMINATE","WSManSignalShell","WSManSignalShell function [Windows Remote Management]","winrm.wsmansignalshell","wsman/WSManSignalShell"]
old-location: winrm\wsmansignalshell.htm
tech.root: winrm
ms.assetid: 9954097d-3e27-4f56-bf8c-3d9aba5c19b5
ms.date: 12/05/2018
ms.keywords: WSMAN_SIGNAL_SHELL_CODE_CTRL_BREAK, WSMAN_SIGNAL_SHELL_CODE_CTRL_C, WSMAN_SIGNAL_SHELL_CODE_TERMINATE, WSManSignalShell, WSManSignalShell function [Windows Remote Management], winrm.wsmansignalshell, wsman/WSManSignalShell
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManSignalShell
 - wsman/WSManSignalShell
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManSignalShell
---

# WSManSignalShell function


## -description

Sends a control code to an existing command or to the shell itself.

## -parameters

### -param shell [in]

Specifies the handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.

### -param command [in, optional]

Specifies the command handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a> call. If this value is <b>NULL</b>, the signal code is sent to the shell.

### -param flags

Reserved for future use. Must be set to zero.

### -param code [in]

Specifies the signal code to send to the command or shell.
The following codes are common.



#### WSMAN_SIGNAL_SHELL_CODE_TERMINATE

The shell or Command Prompt window was closed.



#### WSMAN_SIGNAL_SHELL_CODE_CTRL_C

The signal for CTRL+C was received, and the process was halted.



#### WSMAN_SIGNAL_SHELL_CODE_CTRL_BREAK

The signal for CTRL+BREAK was received, and the process was halted.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information.  This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseoperation">WSManCloseOperation</a> method.

### -param signalOperation [out]

Defines the operation handle for the signal operation. This handle is returned from a successful call of the function and can be used to asynchronously cancel the signal operation. This handle should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseoperation">WSManCloseOperation</a> method. This parameter cannot be <b>NULL</b>.