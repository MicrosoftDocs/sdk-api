---
UID: NC:wsman.WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
title: WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT (wsman.h)
description: Defines the release shell callback for the plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT","WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback","WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback function [Windows Remote Management]","WSManPluginReleaseCommandContext","winrm.wsman_plugin_release_shell_context","wsman/WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT"]
old-location: winrm\wsman_plugin_release_shell_context.htm
tech.root: winrm
ms.assetid: 8cb33e6c-fc64-4aad-88b3-9faeef3809c4
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT, WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback, WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback function [Windows Remote Management], WSManPluginReleaseCommandContext, winrm.wsman_plugin_release_shell_context, wsman/WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
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
 - WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
 - wsman/WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
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
 - WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT
---

# WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback function


## -description

Defines the release shell callback for the plug-in. This function is called to delete the plug-in shell context.

The DLL entry point name must be <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_release_command_context">WSManPluginReleaseCommandContext</a>.

## -parameters

### -param shellContext [in]

Specifies the context that was received when the shell was created.