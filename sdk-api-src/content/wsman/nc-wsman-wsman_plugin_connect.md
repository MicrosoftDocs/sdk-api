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



