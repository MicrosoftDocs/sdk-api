---
UID: NC:wsman.WSMAN_PLUGIN_RECEIVE
title: WSMAN_PLUGIN_RECEIVE
author: windows-sdk-content
description: Defines the receive callback for a plug-in.
old-location: winrm\wsman_plugin_receive.htm
tech.root: WinRM
ms.assetid: 59dff87b-17d5-4875-ad24-1520a04b05d2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSMAN_PLUGIN_RECEIVE, WSMAN_PLUGIN_RECEIVE callback, WSMAN_PLUGIN_RECEIVE callback function [Windows Remote Management], WSManPluginReceive, winrm.wsman_plugin_receive, wsman/WSMAN_PLUGIN_RECEIVE
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
 - WSMAN_PLUGIN_RECEIVE
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# WSMAN_PLUGIN_RECEIVE callback function


## -description


Defines the receive callback for a plug-in. This function is called when an inbound request to receive data is received.

The DLL entry point name must be <b>WSManPluginReceive</b>.


## -parameters




### -param *requestDetails

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags

Reserved for future use. Must be zero.


### -param shellContext

Specifies the context that was received when the shell was created.


### -param commandContext

If this request is aimed at a command and not a shell, this is the context returned from the <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.


### -param *streamSet

A <a href="https://msdn.microsoft.com/a5705afa-e0b3-4a74-8c13-5abf3f53a209">WSMAN_STREAM_ID_SET</a> structure that contains a list of streams for which  data is to be received.  If this list is empty, all streams that were configured in the shell are implied, which means  that all streams are available.


## -returns



This callback function does not return a value.




## -remarks



Based on the client request, the <b>WSMAN_PLUGIN_RECEIVE</b> callback function can be called against the shell and/or the command. The plug-in calls the <a href="https://msdn.microsoft.com/717c1e37-83e1-4caf-8b52-175999597fc0">WSManPluginReceiveResult</a> method for each piece of data that needs to be sent back to the client. After all of the data has been sent, the plug-in calls <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a> to end the stream. All parameters passed in are valid until the Windows Remote Management (WinRM) plug-in calls <b>WSManPluginOperationComplete</b>.



