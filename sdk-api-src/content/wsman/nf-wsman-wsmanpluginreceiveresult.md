---
UID: NF:wsman.WSManPluginReceiveResult
title: WSManPluginReceiveResult function
author: windows-sdk-content
description: Reports results for the WSMAN_PLUGIN_RECEIVE plug-in call and is used by most shell plug-ins that return results.
old-location: winrm\wsmanpluginreceiveresult.htm
tech.root: winrm
ms.assetid: 717c1e37-83e1-4caf-8b52-175999597fc0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSMAN_RECEIVE_STATE_ABNORMAL_TERMINATION, WSMAN_RECEIVE_STATE_INPUT_REQUIRED, WSMAN_RECEIVE_STATE_NONE, WSMAN_RECEIVE_STATE_NORMAL_TERMINATION, WSMAN_RECEIVE_STATE_WAITING, WSManPluginReceiveResult, WSManPluginReceiveResult function [Windows Remote Management], winrm.wsmanpluginreceiveresult, wsman/WSManPluginReceiveResult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManPluginReceiveResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
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

