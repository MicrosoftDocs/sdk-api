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

# WSManPluginReceiveResult function


## -description


Reports results for the <a href="https://msdn.microsoft.com/59dff87b-17d5-4875-ad24-1520a04b05d2">WSMAN_PLUGIN_RECEIVE</a> plug-in call and  is used by most shell plug-ins that return results.  After  all of the data is received,
the <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a> method must be called.


## -parameters




### -param requestDetails [in]

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags [in]

Reserved for future use. Must be set to zero.


### -param stream [in, optional]

Specifies the stream that the data is associated with. Any stream can be used, but the standard streams are STDIN, STDOUT, and STDERR.


### -param streamResult [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that specifies the result object that is returned to the client. The result can be in either binary or XML format.


### -param commandState [in, optional]

Specifies the state of the command. This parameter must be set either to one of the following values or to a value defined by the plug-in.



#### WSMAN_RECEIVE_STATE_NONE

The operation requires no action.



#### WSMAN_RECEIVE_STATE_NORMAL_TERMINATION

The operation was terminated normally.



#### WSMAN_RECEIVE_STATE_ABNORMAL_TERMINATION

The operation was terminated unexpectedly.



#### WSMAN_RECEIVE_STATE_WAITING

The operation is waiting for input.



#### WSMAN_RECEIVE_STATE_INPUT_REQUIRED

The operation requires command-line input.


### -param exitCode [in]

Ignored in all cases except when <i>commandState</i> is either <b>WSMAN_RECEIVE_STATE_NORMAL_TERMINATION</b> or <b>WSMAN_RECEIVE_STATE_ABNORMAL_TERMINATION</b>. Each result can have separate error codes. If the command or stream has failed, the plug-in must call the <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a> method.

