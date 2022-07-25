---
UID: NC:wsman.WSMAN_PLUGIN_SHELL
title: WSMAN_PLUGIN_SHELL (wsman.h)
description: Defines the shell callback for a plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_SHELL","WSMAN_PLUGIN_SHELL callback","WSMAN_PLUGIN_SHELL callback function [Windows Remote Management]","WSManPluginShell","winrm.wsman_plugin_shell","wsman/WSMAN_PLUGIN_SHELL"]
old-location: winrm\wsman_plugin_shell.htm
tech.root: winrm
ms.assetid: 3016612a-ce99-405b-afae-200bcad9ed20
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_SHELL, WSMAN_PLUGIN_SHELL callback, WSMAN_PLUGIN_SHELL callback function [Windows Remote Management], WSManPluginShell, winrm.wsman_plugin_shell, wsman/WSMAN_PLUGIN_SHELL
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSMAN_PLUGIN_SHELL
 - wsman/WSMAN_PLUGIN_SHELL
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
 - WSMAN_PLUGIN_SHELL
---

# WSMAN_PLUGIN_SHELL callback function


## -description

Defines the shell callback for a plug-in. This function is called when a request for a new shell is received.  All Windows Remote Management plug-ins that support shell operations need to implement this callback.

The DLL entry point name must be <b>WSManPluginShell</b>.

## -parameters

### -param pluginContext

Specifies the context that was returned by a call to the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a> method. This parameter represents a specific application initialization of a WinRM plug-in.

### -param requestDetails

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags

Reserved for future use. Must be set to zero.

### -param startupInfo

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_startup_info_v10">WSMAN_SHELL_STARTUP_INFO</a> structure that contains startup information for the shell.

### -param inboundShellInformation

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that specifies an optional inbound object that contains extra data for the shell.

## -remarks

The WinRM (WinRM) plug-in calls <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginreportcontext">WSManPluginReportContext</a> to register a shell context for the shell. All operations on this shell pass into this context. If the shell has shut down or the plug-in checks the  <i>requestDetails</i> parameter and reports that the operation was  canceled, the plug-in should call <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a>.  All parameters passed in are valid until the WinRM plug-in calls <b>WSManPluginOperationComplete</b>.
