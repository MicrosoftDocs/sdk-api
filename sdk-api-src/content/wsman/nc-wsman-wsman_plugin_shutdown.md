---
UID: NC:wsman.WSMAN_PLUGIN_SHUTDOWN
title: WSMAN_PLUGIN_SHUTDOWN (wsman.h)
description: Defines the shutdown callback for the plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_SHUTDOWN","WSMAN_PLUGIN_SHUTDOWN callback","WSMAN_PLUGIN_SHUTDOWN callback function [Windows Remote Management]","WSMAN_PLUGIN_SHUTDOWN_IISHOST","WSMAN_PLUGIN_SHUTDOWN_SERVICE","WSMAN_PLUGIN_SHUTDOWN_SYSTEM","WSManPluginShutdown","winrm.wsman_plugin_shutdown","wsman/WSMAN_PLUGIN_SHUTDOWN"]
old-location: winrm\wsman_plugin_shutdown.htm
tech.root: winrm
ms.assetid: a9f72416-f6a7-4ba0-94d0-48f85393acab
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_SHUTDOWN, WSMAN_PLUGIN_SHUTDOWN callback, WSMAN_PLUGIN_SHUTDOWN callback function [Windows Remote Management], WSMAN_PLUGIN_SHUTDOWN_IISHOST, WSMAN_PLUGIN_SHUTDOWN_SERVICE, WSMAN_PLUGIN_SHUTDOWN_SYSTEM, WSManPluginShutdown, winrm.wsman_plugin_shutdown, wsman/WSMAN_PLUGIN_SHUTDOWN
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2, , and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSMAN_PLUGIN_SHUTDOWN
 - wsman/WSMAN_PLUGIN_SHUTDOWN
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
 - WSMAN_PLUGIN_SHUTDOWN
---

# WSMAN_PLUGIN_SHUTDOWN callback function


## -description

Defines the shutdown callback for the plug-in. This function is called after all operations have been canceled and before the Windows Remote Management plug-in DLL is unloaded. All WinRM plug-ins must implement this callback function.

The DLL entry point name must be <b>WSManPluginShutdown</b>.

## -parameters

### -param pluginContext

Specifies the context that was returned by a call to the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a> method. This parameter represents a specific application initialization of a WinRM plug-in. The shutdown entry point will be called for each application that initialized it.

### -param flags

Reserved for future use. Must be set to zero.

### -param reason

Specifies the reason that the plug-in is shutting down.



#### WSMAN_PLUGIN_SHUTDOWN_SYSTEM

The system shut down.



#### WSMAN_PLUGIN_SHUTDOWN_SERVICE

The WinRM service shut down.



#### WSMAN_PLUGIN_SHUTDOWN_IISHOST

The IIS host shut down.

## -returns

The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code.

<div class="alert"><b>Note</b>  If this method fails, the plug-in will not call back in.</div>
<div> </div>

## -remarks

Each successful call to <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a> will result in a call to this function before the WinRM plug-in DLL is unloaded. It is important to ensure that the WinRM plug-in tracks the number of times that this startup entry point is called so that the plug-in is not shut down prematurely.

This function must ensure that all plug-in threads are shut down before it returns. If the plug-in handles only synchronous operations and all threads report a cancellation result before they return, this function performs only plug-in cleanup. However, for an asynchronous plug-in, any threads that are used to process the plug-in threads, including the ones that just reported the cancellation for all operations, need to be completely shut down. If all of the threads are not shut down, crashes in the DLL might occur because code might be executed after the DLL is unloaded.