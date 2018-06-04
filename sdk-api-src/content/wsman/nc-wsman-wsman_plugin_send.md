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

# WSMAN_PLUGIN_SEND callback function


## -description


Defines the send callback for a plug-in. This function is called for each object that is received from a client.  Each object received causes the callback to be called once.
After the data is processed, the Windows Remote Management (WinRM) plug-in calls <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a> to acknowledge receipt and to allow the next object to be delivered.

The DLL entry point name must be <b>WSManPluginSend</b>.


## -parameters




### -param *requestDetails

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags

If this is the last object for the stream, this parameter is set to <b>WSMAN_FLAG_NO_MORE_DATA</b>.
Otherwise, it is set to zero.


### -param shellContext

Specifies the context that was received when the shell was created.


### -param commandContext

If this request is aimed at a command and not a shell, this is the context returned from the <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.


### -param stream

Specifies the stream that is associated with the inbound object.


### -param *inboundData

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that contains data being sent to the specified stream. It is in the form of binary data.


## -returns



This callback function does not return a value.



