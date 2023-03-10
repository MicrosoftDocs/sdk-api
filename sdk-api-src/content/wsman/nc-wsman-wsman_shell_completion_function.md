---
UID: NC:wsman.WSMAN_SHELL_COMPLETION_FUNCTION
title: WSMAN_SHELL_COMPLETION_FUNCTION (wsman.h)
description: The callback function that is called for shell operations, which result in a remote request.
helpviewer_keywords: ["WSMAN_SHELL_COMPLETION_FUNCTION","WSMAN_SHELL_COMPLETION_FUNCTION callback","WSMAN_SHELL_COMPLETION_FUNCTION callback function [Windows Remote Management]","winrm.wsman_shell_completion_function","wsman/WSMAN_SHELL_COMPLETION_FUNCTION"]
old-location: winrm\wsman_shell_completion_function.htm
tech.root: winrm
ms.assetid: 705732a8-7584-42cf-be9b-dd36b35bba37
ms.date: 12/05/2018
ms.keywords: WSMAN_SHELL_COMPLETION_FUNCTION, WSMAN_SHELL_COMPLETION_FUNCTION callback, WSMAN_SHELL_COMPLETION_FUNCTION callback function [Windows Remote Management], winrm.wsman_shell_completion_function, wsman/WSMAN_SHELL_COMPLETION_FUNCTION
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, and     Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSMAN_SHELL_COMPLETION_FUNCTION
 - wsman/WSMAN_SHELL_COMPLETION_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_COMPLETION_FUNCTION
---

# WSMAN_SHELL_COMPLETION_FUNCTION callback function


## -description

The callback function that is called for shell operations, which result in a remote request.

## -parameters

### -param operationContext [in, optional]

Represents user-defined context passed to the WinRM (WinRM) Client Shell 
      application programming interface (API) .

### -param flags

Specifies one or more flags from the 
      <a href="/windows/desktop/api/wsman/ne-wsman-wsmancallbackflags">WSManCallbackFlags</a> enumeration.

### -param error [in]

Defines the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_error">WSMAN_ERROR</a> structure, which is 
      valid in the callback only.

### -param shell [in]

Specifies the shell handle  associated with the user context.  The shell handle  must be closed by calling 
      the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseshell">WSManCloseShell</a> method.

### -param command [in, optional]

Specifies the command handle associated with the user context. The command handle must be closed by calling 
      the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> API method.

### -param operationHandle [in, optional]

Defines the operation handle associated with the user context. The operation handle is valid only for 
      callbacks that are associated with 
      <a href="/windows/desktop/api/wsman/nf-wsman-wsmanreceiveshelloutput">WSManReceiveShellOutput</a>, 
      <a href="/windows/desktop/api/wsman/nf-wsman-wsmansendshellinput">WSManSendShellInput</a>, and 
      <a href="/windows/desktop/api/wsman/nf-wsman-wsmansignalshell">WSManSignalShell</a> calls. This handle must be closed 
      by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseoperation">WSManCloseOperation</a> 
      method.

### -param data [in, optional]

Defines the output data from the command or shell as a result of a 
      <a href="/windows/desktop/api/wsman/nf-wsman-wsmanreceiveshelloutput">WSManReceiveShellOutput</a> call. For more 
      information about the output data, see the 
      <a href="/windows/desktop/api/wsman/ns-wsman-wsman_receive_data_result">WSMAN_RECEIVE_DATA_RESULT</a> structure.
