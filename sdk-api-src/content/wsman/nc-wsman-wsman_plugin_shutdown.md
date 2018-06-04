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

# WSMAN_PLUGIN_SHUTDOWN callback function


## -description


Defines the shutdown callback for the plug-in. This function is called after all operations have been canceled and before the Windows Remote Management plug-in DLL is unloaded. All WinRM plug-ins must implement this callback function.

The DLL entry point name must be <b>WSManPluginShutdown</b>.


## -parameters




### -param pluginContext

Specifies the context that was returned by a call to the <a href="https://msdn.microsoft.com/b3123f52-880b-4d14-a5a2-77c5924de99d">WSManPluginStartup</a> method. This parameter represents a specific application initialization of a WinRM plug-in. The shutdown entry point will be called for each application that initialized it.


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



Each successful call to <a href="https://msdn.microsoft.com/b3123f52-880b-4d14-a5a2-77c5924de99d">WSManPluginStartup</a> will result in a call to this function before the WinRM plug-in DLL is unloaded. It is important to ensure that the WinRM plug-in tracks the number of times that this startup entry point is called so that the plug-in is not shut down prematurely.

This function must ensure that all plug-in threads are shut down before it returns. If the plug-in handles only synchronous operations and all threads report a cancellation result before they return, this function performs only plug-in cleanup. However, for an asynchronous plug-in, any threads that are used to process the plug-in threads, including the ones that just reported the cancellation for all operations, need to be completely shut down. If all of the threads are not shut down, crashes in the DLL might occur because code might be executed after the DLL is unloaded.



