---
UID: NF:wsman.WSManCreateShellEx
title: WSManCreateShellEx function (wsman.h)
description: Creates a shell object by using the same functionality as the WSManCreateShell function, with the addition of a client-specified shell ID.
helpviewer_keywords: ["WSManCreateShellEx","WSManCreateShellEx function [Windows Remote Management]","winrm.wsmancreateshellex","wsman/WSManCreateShellEx"]
old-location: winrm\wsmancreateshellex.htm
tech.root: winrm
ms.assetid: A339FC95-2235-4102-A0FC-7FB01132B7A1
ms.date: 12/05/2018
ms.keywords: WSManCreateShellEx, WSManCreateShellEx function [Windows Remote Management], winrm.wsmancreateshellex, wsman/WSManCreateShellEx
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
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSManCreateShellEx
 - wsman/WSManCreateShellEx
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
 - WSManCreateShellEx
---

# WSManCreateShellEx function


## -description

Creates a shell object by using the same functionality as the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> function, with the addition of a client-specified shell ID. The returned shell handle identifies an object that defines the context in which commands can be run. The context is defined by the environment variables, the input and output streams, and the working directory. The context can directly affect the behavior of a command. A shell context is created on the remote computer specified by the connection parameter and authenticated by using the credentials parameter.

## -parameters

### -param session [in, out]

Specifies the session handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreatesession">WSManCreateSession</a> call. This parameter cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be 0.

### -param resourceUri [in]

Defines the shell type to create. The shell type is defined by a unique URI. The actual shell object returned by the call is dependent on the URI specified. This parameter cannot be <b>NULL</b>. To create a Windows cmd.exe shell, use the <b>WSMAN_CMDSHELL_URI</b> resource URI.

### -param shellId [in]

The client specified <i>shellID</i>.

### -param startupInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_startup_info_v10">WSMAN_SHELL_STARTUP_INFO</a> structure that specifies the input and output streams, working directory, idle timeout, and options for the shell. If this parameter is <b>NULL</b>, the default values will be used.

### -param options [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_option_set">WSMAN_OPTION_SET</a> structure that specifies a set of options for the shell.

### -param createXml [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that defines an open context for the shell. The content should be a valid XML string. This parameter can be <b>NULL</b>.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseshell">WSManCloseShell</a> method.

### -param shell [out]

Defines a shell handle that uniquely identifies the shell object. The resource handle is used to track the client endpoint for the shell and is used by other WinRM methods to interact with the shell object. The shell object should be deleted by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseshell">WSManCloseShell</a> method. This parameter cannot be <b>NULL</b>.