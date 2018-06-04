---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



