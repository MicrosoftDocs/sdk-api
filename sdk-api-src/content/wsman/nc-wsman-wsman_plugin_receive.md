---
UID: NC:wsman.WSMAN_PLUGIN_RECEIVE
title: WSMAN_PLUGIN_RECEIVE (wsman.h)
description: Defines the receive callback for a plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_RECEIVE","WSMAN_PLUGIN_RECEIVE callback","WSMAN_PLUGIN_RECEIVE callback function [Windows Remote Management]","WSManPluginReceive","winrm.wsman_plugin_receive","wsman/WSMAN_PLUGIN_RECEIVE"]
old-location: winrm\wsman_plugin_receive.htm
tech.root: winrm
ms.assetid: 59dff87b-17d5-4875-ad24-1520a04b05d2
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_RECEIVE, WSMAN_PLUGIN_RECEIVE callback, WSMAN_PLUGIN_RECEIVE callback function [Windows Remote Management], WSManPluginReceive, winrm.wsman_plugin_receive, wsman/WSMAN_PLUGIN_RECEIVE
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
 - WSMAN_PLUGIN_RECEIVE
 - wsman/WSMAN_PLUGIN_RECEIVE
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
 - WSMAN_PLUGIN_RECEIVE
---

# WSMAN_PLUGIN_RECEIVE callback function


## -description

Defines the receive callback for a plug-in. This function is called when an inbound request to receive data is received.

The DLL entry point name must be <b>WSManPluginReceive</b>.

## -parameters

### -param requestDetails

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags

Reserved for future use. Must be zero.

### -param shellContext

Specifies the context that was received when the shell was created.

### -param commandContext

If this request is aimed at a command and not a shell, this is the context returned from the <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.

### -param streamSet

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_stream_id_set">WSMAN_STREAM_ID_SET</a> structure that contains a list of streams for which  data is to be received.  If this list is empty, all streams that were configured in the shell are implied, which means  that all streams are available.

## -remarks

Based on the client request, the <b>WSMAN_PLUGIN_RECEIVE</b> callback function can be called against the shell and/or the command. The plug-in calls the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginreceiveresult">WSManPluginReceiveResult</a> method for each piece of data that needs to be sent back to the client. After all of the data has been sent, the plug-in calls <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> to end the stream. All parameters passed in are valid until the Windows Remote Management (WinRM) plug-in calls <b>WSManPluginOperationComplete</b>.
