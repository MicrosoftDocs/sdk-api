---
UID: NC:wsman.WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
title: WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
author: windows-sdk-content
description: Defines the release shell callback for the plug-in.
old-location: winrm\wsman_plugin_release_shell_context.htm
tech.root: winrm
ms.assetid: 8cb33e6c-fc64-4aad-88b3-9faeef3809c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT, WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback, WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback function [Windows Remote Management], WSManPluginReleaseCommandContext, winrm.wsman_plugin_release_shell_context, wsman/WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback function


## -description


Defines the release shell callback for the plug-in. This function is called to delete the plug-in shell context.

The DLL entry point name must be <a href="https://msdn.microsoft.com/9a81f8da-1c71-4eab-aa21-002cee4f1164">WSManPluginReleaseCommandContext</a>.


## -parameters




### -param shellContext [in]

Specifies the context that was received when the shell was created.


## -returns



This callback function does not return a value.



