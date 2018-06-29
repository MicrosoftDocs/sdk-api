---
UID: NC:wsman.WSMAN_PLUGIN_SHELL
title: WSMAN_PLUGIN_SHELL
author: windows-sdk-content
description: Defines the shell callback for a plug-in.
old-location: winrm\wsman_plugin_shell.htm
old-project: WinRM
ms.assetid: 3016612a-ce99-405b-afae-200bcad9ed20
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: WSMAN_PLUGIN_SHELL, WSMAN_PLUGIN_SHELL callback, WSMAN_PLUGIN_SHELL callback function [Windows Remote Management], WSManPluginShell, winrm.wsman_plugin_shell, wsman/WSMAN_PLUGIN_SHELL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - WSMAN_PLUGIN_SHELL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSMAN_PLUGIN_SHELL callback function


## -description


Defines the shell callback for a plug-in. This function is called when a request for a new shell is received.  All Windows Remote Management plug-ins that support shell operations need to implement this callback.

The DLL entry point name must be <b>WSManPluginShell</b>.


## -parameters




### -param pluginContext

Specifies the context that was returned by a call to the <a href="https://msdn.microsoft.com/b3123f52-880b-4d14-a5a2-77c5924de99d">WSManPluginStartup</a> method. This parameter represents a specific application initialization of a WinRM plug-in.


### -param *requestDetails

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags

Reserved for future use. Must be set to zero.


### -param *startupInfo

A pointer to a <a href="https://msdn.microsoft.com/a9e004de-b157-4ad3-a463-a42ccb56f1ba">WSMAN_SHELL_STARTUP_INFO</a> structure that contains startup information for the shell.


### -param *inboundShellInformation

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that specifies an optional inbound object that contains extra data for the shell.


## -returns



This callback function does not return a value.




## -remarks



The WinRM (WinRM) plug-in calls <a href="https://msdn.microsoft.com/8bdfeabf-1028-4ddb-8953-455bbc2a1a1e">WSManPluginReportContext</a> to register a shell context for the shell. All operations on this shell pass into this context. If the shell has shut down or the plug-in checks the  <i>requestDetails</i> parameter and reports that the operation was  canceled, the plug-in should call <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a>.  All parameters passed in are valid until the WinRM plug-in calls <b>WSManPluginOperationComplete</b>.



