---
UID: NC:wsman.WSMAN_PLUGIN_STARTUP
title: WSMAN_PLUGIN_STARTUP (wsman.h)
description: Defines the startup callback for the plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_STARTUP","WSMAN_PLUGIN_STARTUP callback","WSMAN_PLUGIN_STARTUP callback function [Windows Remote Management]","WSManPluginStartup","winrm.wsman_plugin_startup","wsman/WSMAN_PLUGIN_STARTUP"]
old-location: winrm\wsman_plugin_startup.htm
tech.root: winrm
ms.assetid: b3123f52-880b-4d14-a5a2-77c5924de99d
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_STARTUP, WSMAN_PLUGIN_STARTUP callback, WSMAN_PLUGIN_STARTUP callback function [Windows Remote Management], WSManPluginStartup, winrm.wsman_plugin_startup, wsman/WSMAN_PLUGIN_STARTUP
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
 - WSMAN_PLUGIN_STARTUP
 - wsman/WSMAN_PLUGIN_STARTUP
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
 - WSMAN_PLUGIN_STARTUP
---

# WSMAN_PLUGIN_STARTUP callback function


## -description

Defines the startup callback for the plug-in. Because multiple applications can be hosted in the same process, this method can be called multiple times, but only once for each application initialization. A plug-in can be initialized more than once within the same process but only once for each <i>applicationIdentification</i> value. The context that is returned from this method should be application specific. The returned context will be passed into all future plug-in calls that are specific to the application. All Windows Remote Management (WinRM) plug-ins must implement this callback function.

The DLL entry point name for this method must be <b>WSManPluginStartup</b>.

## -parameters

### -param flags

Reserved for future use. Must be zero.

### -param applicationIdentification

A unique identifier for the hosted application. For the main WinRM service, the default is <b>wsman</b>. For an Internet Information Services (IIS) host, this identifier is related to the application endpoint for that host. For example, <b>wsman/MyCompany/MyApplication</b>.

### -param extraInfo

A string that contains configuration information, if any information was stored when the plug-in was registered. When the plug-in is registered using the WinRM configuration, the plug-in can add extra configuration parameters that are useful during initialization to an optional node.  This information can be especially useful if a plug-in is used in different IIS hosting scenarios and requires slightly different run-time semantics during initialization.  This string is a copy of the XML from the configuration, if one is present.  Otherwise, this parameter is set to <b>NULL</b>.

### -param pluginContext

The context for the specific application initialization.  This context is passed through to all other WinRM plug-in calls that are associated with this <i>applicationIdentifier</i>.

## -returns

The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code.  If this method returns an error, the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_shutdown">WSManPluginShutdown</a> entry point will not be called.
