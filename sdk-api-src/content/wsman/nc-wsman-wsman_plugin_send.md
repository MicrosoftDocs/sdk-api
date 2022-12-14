---
UID: NC:wsman.WSMAN_PLUGIN_SEND
title: WSMAN_PLUGIN_SEND (wsman.h)
description: Defines the send callback for a plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_SEND","WSMAN_PLUGIN_SEND callback","WSMAN_PLUGIN_SEND callback function [Windows Remote Management]","WSManPluginSend","winrm.wsman_plugin_send","wsman/WSMAN_PLUGIN_SEND"]
old-location: winrm\wsman_plugin_send.htm
tech.root: winrm
ms.assetid: d287915b-9af9-4b87-9456-224e96e6dc20
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_SEND, WSMAN_PLUGIN_SEND callback, WSMAN_PLUGIN_SEND callback function [Windows Remote Management], WSManPluginSend, winrm.wsman_plugin_send, wsman/WSMAN_PLUGIN_SEND
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
 - WSMAN_PLUGIN_SEND
 - wsman/WSMAN_PLUGIN_SEND
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
 - WSMAN_PLUGIN_SEND
---

# WSMAN_PLUGIN_SEND callback function


## -description

Defines the send callback for a plug-in. This function is called for each object that is received from a client.  Each object received causes the callback to be called once.
After the data is processed, the Windows Remote Management (WinRM) plug-in calls <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> to acknowledge receipt and to allow the next object to be delivered.

The DLL entry point name must be <b>WSManPluginSend</b>.

## -parameters

### -param requestDetails

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags

If this is the last object for the stream, this parameter is set to <b>WSMAN_FLAG_NO_MORE_DATA</b>.
Otherwise, it is set to zero.

### -param shellContext

Specifies the context that was received when the shell was created.

### -param commandContext

If this request is aimed at a command and not a shell, this is the context returned from the <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.

### -param stream

Specifies the stream that is associated with the inbound object.

### -param inboundData

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that contains data being sent to the specified stream. It is in the form of binary data.
