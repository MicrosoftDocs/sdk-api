---
UID: NF:wsman.WSManCloseShell
title: WSManCloseShell function (wsman.h)
description: Deletes a shell object and frees the resources associated with the shell.
helpviewer_keywords: ["WSManCloseShell","WSManCloseShell function [Windows Remote Management]","winrm.wsmancloseshell","wsman/WSManCloseShell"]
old-location: winrm\wsmancloseshell.htm
tech.root: winrm
ms.assetid: 1da452ef-5842-4d8d-941b-09fa57393ebb
ms.date: 12/05/2018
ms.keywords: WSManCloseShell, WSManCloseShell function [Windows Remote Management], winrm.wsmancloseshell, wsman/WSManCloseShell
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManCloseShell
 - wsman/WSManCloseShell
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
 - WSManCloseShell
---

# WSManCloseShell function


## -description

Deletes a shell object and frees the resources associated with the shell.

## -parameters

### -param shellHandle [in, out, optional]

Specifies the shell handle to close. This handle is returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be set to zero.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information.  This parameter cannot be <b>NULL</b>.