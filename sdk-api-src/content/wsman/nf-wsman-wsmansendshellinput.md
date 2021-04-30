---
UID: NF:wsman.WSManSendShellInput
title: WSManSendShellInput function (wsman.h)
description: Ipes the input stream to a running command or to the shell.
helpviewer_keywords: ["WSManSendShellInput","WSManSendShellInput function [Windows Remote Management]","winrm.wsmansendshellinput","wsman/WSManSendShellInput"]
old-location: winrm\wsmansendshellinput.htm
tech.root: winrm
ms.assetid: 2336671e-0f60-407f-86a2-9918bbf7f66b
ms.date: 12/05/2018
ms.keywords: WSManSendShellInput, WSManSendShellInput function [Windows Remote Management], winrm.wsmansendshellinput, wsman/WSManSendShellInput
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
 - WSManSendShellInput
 - wsman/WSManSendShellInput
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
 - WSManSendShellInput
---

# WSManSendShellInput function


## -description

Pipes the  input stream to a running command or to the shell.

## -parameters

### -param shell [in]

Specifies the shell handle returned by a  <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.

### -param command [in, optional]

Specifies the command handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a> call.  This handle  should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method.

### -param flags

Reserved for future use. Must be set to zero.

### -param streamId [in]

Specifies the input stream ID. This parameter cannot be <b>NULL</b>.

### -param streamData [in]

Uses the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure to specify the stream data to be sent to the command or shell. This structure should be allocated by the calling client and must remain allocated until <b>WSManSendShellInput</b> completes. If the end of the stream has been reached, the <i>endOfStream</i> parameter should be set to <b>TRUE</b>.

### -param endOfStream

Set to <b>TRUE</b>, if the end of the stream has been reached. Otherwise, this parameter is set to <b>FALSE</b>.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method.

### -param sendOperation [out]

Defines the operation handle for the send operation. This handle is returned from a successful call of the function and can be used to asynchronously cancel the send operation. This handle should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseoperation">WSManCloseOperation</a> method. This parameter cannot be <b>NULL</b>.