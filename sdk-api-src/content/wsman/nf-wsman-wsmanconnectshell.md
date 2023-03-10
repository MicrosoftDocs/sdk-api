---
UID: NF:wsman.WSManConnectShell
title: WSManConnectShell function (wsman.h)
description: Connects to an existing server session.
helpviewer_keywords: ["WSManConnectShell","WSManConnectShell function [Windows Remote Management]","winrm.wsmanconnectshell","wsman/WSManConnectShell"]
old-location: winrm\wsmanconnectshell.htm
tech.root: winrm
ms.assetid: B765AB84-5EDA-46D6-9150-A8BBD101EF10
ms.date: 12/05/2018
ms.keywords: WSManConnectShell, WSManConnectShell function [Windows Remote Management], winrm.wsmanconnectshell, wsman/WSManConnectShell
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
req.redist: WinRM on Windows Server 2012.
ms.custom: 19H1
f1_keywords:
 - WSManConnectShell
 - wsman/WSManConnectShell
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
 - WSManConnectShell
---

# WSManConnectShell function


## -description

Connects to an existing server session.

## -parameters

### -param session [in, out]

Specifies the session handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreatesession">WSManCreateSession</a> function. This parameter cannot be NULL.

### -param flags

Reserved for future use. Must be zero.

### -param resourceUri [in]

Defines the shell type  to which the connection will be made. The shell type is defined by a unique URI, therefore the shell object returned by the call is dependent on the URI that is specified by this parameter. The <i>resourceUri</i> parameter cannot be NULL and it is a null-terminated string.

### -param shellID [in]

Specifies the shell identifier that is associated with the server shell session to which the client intends to connect.

### -param options [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_option_set">WSMAN_OPTION_SET</a> structure that specifies a set of options for the shell. This parameter is optional.

### -param connectXml [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that defines an open context for the connect shell operation. The content should be a valid XML string. This parameter can be NULL.

### -param async [in]

Defines an asynchronous structure that contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be NULL.

### -param shell [out]

Specifies a shell handle that uniquely identifies the shell object that was returned by <i>resourceURI</i>. The resource handle tracks the client endpoint for the shell and is used by other WinRM methods to interact with the shell object. The shell object should be deleted by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseshell">WSManCloseShell</a> method. This parameter cannot be NULL.

## -remarks

Connects to an existing server shell session identified by the <i>ShellId</i> parameter. This builds the necessary client side context, represented by the return parameter shell, that can be used to carry out subsequent operations such as running commands and sending and receiving output on the server shell session. 
This <b>WSManConnectShell</b> function does not automatically construct the client side contexts for any commands that are currently associated with the server shell session.