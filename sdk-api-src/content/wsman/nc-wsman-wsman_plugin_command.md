---
UID: NC:wsman.WSMAN_PLUGIN_COMMAND
title: WSMAN_PLUGIN_COMMAND (wsman.h)
description: Defines the command callback for a plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_COMMAND","WSMAN_PLUGIN_COMMAND callback","WSMAN_PLUGIN_COMMAND callback function [Windows Remote Management]","WSManPluginCommand","winrm.wsman_plugin_command","wsman/WSMAN_PLUGIN_COMMAND"]
old-location: winrm\wsman_plugin_command.htm
tech.root: winrm
ms.assetid: df4b4e7b-cf30-4eb0-b646-49b17c883a16
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_COMMAND, WSMAN_PLUGIN_COMMAND callback, WSMAN_PLUGIN_COMMAND callback function [Windows Remote Management], WSManPluginCommand, winrm.wsman_plugin_command, wsman/WSMAN_PLUGIN_COMMAND
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
 - WSMAN_PLUGIN_COMMAND
 - wsman/WSMAN_PLUGIN_COMMAND
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
 - WSMAN_PLUGIN_COMMAND
---

# WSMAN_PLUGIN_COMMAND callback function


## -description

Defines the command callback for a plug-in. This function is called when a request for a command is received. All Windows Remote Management plug-ins that support shell operations and need to create commands must implement this callback.

The DLL entry point name must be <b>WSManPluginCommand</b>.

## -parameters

### -param requestDetails

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags

Reserved for future use. Must be set to zero.

### -param shellContext

Specifies the context returned from creating the shell for which this command needs to be associated.

### -param commandLine

Specifies the command line to be run.

### -param arguments

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_command_arg_set">WSMAN_COMMAND_ARG_SET</a> structure that specifies  the command-line arguments to be passed to the command.

## -remarks

The WinRM (WinRM) plug-in will call the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginreportcontext">WSManPluginReportContext</a> method to register a command context for the command. All operations on this command are passed into this context. The context must be valid until the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> method is called by the plug-in to indicate that either the command is complete or the shell was shut down. All parameters passed in are valid until the WinRM plug-in calls <b>WSManPluginOperationComplete</b>.
