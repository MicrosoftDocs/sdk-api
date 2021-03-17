---
UID: NF:wsman.WSManReceiveShellOutput
title: WSManReceiveShellOutput function (wsman.h)
description: Retrieves output from a running command or from the shell.
helpviewer_keywords: ["WSManReceiveShellOutput","WSManReceiveShellOutput function [Windows Remote Management]","winrm.wsmanreceiveshelloutput","wsman/WSManReceiveShellOutput"]
old-location: winrm\wsmanreceiveshelloutput.htm
tech.root: winrm
ms.assetid: cc64f212-9897-4a58-b3f1-bc2093f593ba
ms.date: 12/05/2018
ms.keywords: WSManReceiveShellOutput, WSManReceiveShellOutput function [Windows Remote Management], winrm.wsmanreceiveshelloutput, wsman/WSManReceiveShellOutput
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
 - WSManReceiveShellOutput
 - wsman/WSManReceiveShellOutput
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
 - WSManReceiveShellOutput
---

# WSManReceiveShellOutput function


## -description

Retrieves output from a running command or from the shell.

## -parameters

### -param shell [in, out]

Specifies the shell handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.

### -param command [in, optional]

Specifies the command handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a> call.

### -param flags

Reserved for future use. Must be set to zero.

### -param desiredStreamSet [in, optional]

Specifies the requested output from a particular stream or a list of streams.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseoperation">WSManCloseOperation</a> method.

### -param receiveOperation [out]

Defines the operation handle for the receive operation. This handle is returned from a successful call of the function and can be used to asynchronously cancel the receive operation. This handle should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseoperation">WSManCloseOperation</a> method. This parameter cannot be <b>NULL</b>.