---
UID: NC:wsman.WSMAN_PLUGIN_CONNECT
title: WSMAN_PLUGIN_CONNECT (wsman.h)
description: Defines the connect callback for a plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_CONNECT","WSMAN_PLUGIN_CONNECT callback","WSMAN_PLUGIN_CONNECT callback function [Windows Remote Management]","WSManPluginConnect","winrm.wsman_plugin_connect","wsman/WSMAN_PLUGIN_CONNECT"]
old-location: winrm\wsman_plugin_connect.htm
tech.root: winrm
ms.assetid: 694C732B-EAA0-4C8A-B3D5-E55ECA5EF733
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_CONNECT, WSMAN_PLUGIN_CONNECT callback, WSMAN_PLUGIN_CONNECT callback function [Windows Remote Management], WSManPluginConnect, winrm.wsman_plugin_connect, wsman/WSMAN_PLUGIN_CONNECT
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
req.redist: Windows Management Framework on Windows Server 2008 and Windows Vista
ms.custom: 19H1
f1_keywords:
 - WSMAN_PLUGIN_CONNECT
 - wsman/WSMAN_PLUGIN_CONNECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WsMan.h
api_name:
 - WSMAN_PLUGIN_CONNECT
---

# WSMAN_PLUGIN_CONNECT callback function


## -description

Defines the connect callback for a plug-in.

The DLL entry point name must be 
    <b>WSManPluginConnect</b>.

## -parameters

### -param requestDetails [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> 
      structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags [in]

Reserved for future use. Must be set to zero.

### -param shellContext [in]

Specifies the context returned from creating the shell for which this connection request needs to be 
      associated.

### -param commandContext [in, optional]

If this request is aimed at a command and not a shell, this is the context returned from the 
      <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.

### -param inboundConnectInformation [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that specifies an 
      optional inbound object that contains extra data for the connection.
