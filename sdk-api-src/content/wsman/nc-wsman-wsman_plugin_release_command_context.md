---
UID: NC:wsman.WSMAN_PLUGIN_RELEASE_COMMAND_CONTEXT
title: WSMAN_PLUGIN_RELEASE_COMMAND_CONTEXT
author: windows-driver-content
description: Defines the release command callback for the plug-in.
old-location: winrm\wsman_plugin_release_command_context.htm
old-project: WinRM
ms.assetid: 9a81f8da-1c71-4eab-aa21-002cee4f1164
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WSManPluginReleaseCommandContext, WSManPluginReleaseCommandContext callback function [Windows Remote Management], winrm.wsman_plugin_release_command_context, wsman/WSMAN_PLUGIN_RELEASE_COMMAND_CONTEXT, wsman/WSManPluginReleaseCommandContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wsman.h
api_name:
-	WSManPluginReleaseCommandContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSMAN_PLUGIN_RELEASE_COMMAND_CONTEXT callback


## -description


Defines the release command callback for the plug-in. This function is called to delete the plug-in command context.

The DLL entry point name must be <b>WSManPluginReleaseCommandContext</b>.


## -parameters




### -param shellContext [in]

Specifies the context that was received when the shell was created.


### -param commandContext [in]

If this request is aimed at a command and not a shell, this is the context returned from the <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.


## -returns



This callback function does not return a value.



