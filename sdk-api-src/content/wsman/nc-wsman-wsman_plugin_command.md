---
UID: NC:wsman.WSMAN_PLUGIN_COMMAND
title: WSMAN_PLUGIN_COMMAND
author: windows-sdk-content
description: Defines the command callback for a plug-in.
old-location: winrm\wsman_plugin_command.htm
old-project: WinRM
ms.assetid: df4b4e7b-cf30-4eb0-b646-49b17c883a16
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSMAN_PLUGIN_COMMAND, WSMAN_PLUGIN_COMMAND callback, WSMAN_PLUGIN_COMMAND callback function [Windows Remote Management], WSManPluginCommand, winrm.wsman_plugin_command, wsman/WSMAN_PLUGIN_COMMAND
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wsman.h
req.include-header: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
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
tech.root: 
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_PLUGIN_COMMAND
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSMAN_PLUGIN_COMMAND callback function


## -description


Defines the command callback for a plug-in. This function is called when a request for a command is received. All Windows Remote Management plug-ins that support shell operations and need to create commands must implement this callback.

The DLL entry point name must be <b>WSManPluginCommand</b>.


## -parameters




### -param *requestDetails

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags

Reserved for future use. Must be set to zero.


### -param shellContext

Specifies the context returned from creating the shell for which this command needs to be associated.


### -param commandLine

Specifies the command line to be run.


### -param *arguments

A pointer to a <a href="https://msdn.microsoft.com/0904851f-e275-445c-b3fa-e5974d037322">WSMAN_COMMAND_ARG_SET</a> structure that specifies  the command-line arguments to be passed to the command.


## -returns



This callback function does not return a value.




## -remarks



The WinRM (WinRM) plug-in will call the <a href="https://msdn.microsoft.com/8bdfeabf-1028-4ddb-8953-455bbc2a1a1e">WSManPluginReportContext</a> method to register a command context for the command. All operations on this command are passed into this context. The context must be valid until the <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a> method is called by the plug-in to indicate that either the command is complete or the shell was shut down. All parameters passed in are valid until the WinRM plug-in calls <b>WSManPluginOperationComplete</b>.



