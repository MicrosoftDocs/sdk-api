---
UID: NC:wsman.WSMAN_PLUGIN_CONNECT
title: WSMAN_PLUGIN_CONNECT
author: windows-sdk-content
description: Defines the connect callback for a plug-in.
old-location: winrm\wsman_plugin_connect.htm
old-project: WinRM
ms.assetid: 694C732B-EAA0-4C8A-B3D5-E55ECA5EF733
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSMAN_PLUGIN_CONNECT, WSMAN_PLUGIN_CONNECT callback, WSMAN_PLUGIN_CONNECT callback function [Windows Remote Management], WSManPluginConnect, winrm.wsman_plugin_connect, wsman/WSMAN_PLUGIN_CONNECT
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WsMan.h
api_name:
 - WSMAN_PLUGIN_CONNECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSMAN_PLUGIN_CONNECT callback function


## -description


Defines the connect callback for a plug-in.

The DLL entry point name must be 
    <b>WSManPluginConnect</b>.


## -parameters




### -param *requestDetails [in]

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> 
      structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags [in]

Reserved for future use. Must be set to zero.


### -param shellContext [in]

Specifies the context returned from creating the shell for which this connection request needs to be 
      associated.


### -param commandContext [in, optional]

If this request is aimed at a command and not a shell, this is the context returned from the 
      <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.


### -param *inboundConnectInformation [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that specifies an 
      optional inbound object that contains extra data for the connection.


## -returns



This callback function does not return a value.



