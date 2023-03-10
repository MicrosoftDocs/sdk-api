---
UID: NS:wsman._WSMAN_SHELL_DISCONNECT_INFO
title: WSMAN_SHELL_DISCONNECT_INFO (wsman.h)
description: Specifies the maximum duration, in milliseconds, the shell will stay open after the client has disconnected.
helpviewer_keywords: ["PWSMAN_SHELL_DISCONNECT_INFO","PWSMAN_SHELL_DISCONNECT_INFO structure pointer [Windows Remote Management]","WSMAN_SHELL_DISCONNECT_INFO","WSMAN_SHELL_DISCONNECT_INFO structure [Windows Remote Management]","winrm.wsman_shell_disconnect_info","wsman/PWSMAN_SHELL_DISCONNECT_INFO","wsman/WSMAN_SHELL_DISCONNECT_INFO"]
old-location: winrm\wsman_shell_disconnect_info.htm
tech.root: winrm
ms.assetid: CFC855E8-25C9-45A1-8D59-55AD5D4A75F3
ms.date: 12/05/2018
ms.keywords: PWSMAN_SHELL_DISCONNECT_INFO, PWSMAN_SHELL_DISCONNECT_INFO structure pointer [Windows Remote Management], WSMAN_SHELL_DISCONNECT_INFO, WSMAN_SHELL_DISCONNECT_INFO structure [Windows Remote Management], winrm.wsman_shell_disconnect_info, wsman/PWSMAN_SHELL_DISCONNECT_INFO, wsman/WSMAN_SHELL_DISCONNECT_INFO
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSMAN_SHELL_DISCONNECT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSMAN_SHELL_DISCONNECT_INFO
 - wsman/_WSMAN_SHELL_DISCONNECT_INFO
 - WSMAN_SHELL_DISCONNECT_INFO
 - wsman/WSMAN_SHELL_DISCONNECT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_DISCONNECT_INFO
---

# WSMAN_SHELL_DISCONNECT_INFO structure


## -description

Specifies the maximum duration, in milliseconds, the shell will stay open after the client has disconnected.

## -struct-fields

### -field idleTimeoutMs

Specifies the maximum time  in milliseconds that the shell will stay open after the client has disconnected. When this maximum duration has been exceeded, the shell will be deleted. Specifying this value overrides the initial idle timeout value that is set as part of the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_startup_info_v10">WSMAN_SHELL_STARTUP_INFO</a> structure in the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> method.

## -remarks

When the maximum duration is exceeded, the shell is automatically deleted. This value overrides the initial idle timeout that is set as part of <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_startup_info_v10">WSMAN_SHELL_STARTUP_INFO</a> structure in <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a>.