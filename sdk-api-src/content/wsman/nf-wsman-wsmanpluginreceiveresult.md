---
UID: NF:wsman.WSManPluginReceiveResult
title: WSManPluginReceiveResult function (wsman.h)
description: Reports results for the WSMAN_PLUGIN_RECEIVE plug-in call and is used by most shell plug-ins that return results.
helpviewer_keywords: ["WSMAN_RECEIVE_STATE_ABNORMAL_TERMINATION","WSMAN_RECEIVE_STATE_INPUT_REQUIRED","WSMAN_RECEIVE_STATE_NONE","WSMAN_RECEIVE_STATE_NORMAL_TERMINATION","WSMAN_RECEIVE_STATE_WAITING","WSManPluginReceiveResult","WSManPluginReceiveResult function [Windows Remote Management]","winrm.wsmanpluginreceiveresult","wsman/WSManPluginReceiveResult"]
old-location: winrm\wsmanpluginreceiveresult.htm
tech.root: winrm
ms.assetid: 717c1e37-83e1-4caf-8b52-175999597fc0
ms.date: 12/05/2018
ms.keywords: WSMAN_RECEIVE_STATE_ABNORMAL_TERMINATION, WSMAN_RECEIVE_STATE_INPUT_REQUIRED, WSMAN_RECEIVE_STATE_NONE, WSMAN_RECEIVE_STATE_NORMAL_TERMINATION, WSMAN_RECEIVE_STATE_WAITING, WSManPluginReceiveResult, WSManPluginReceiveResult function [Windows Remote Management], winrm.wsmanpluginreceiveresult, wsman/WSManPluginReceiveResult
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManPluginReceiveResult
 - wsman/WSManPluginReceiveResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManPluginReceiveResult
---

# WSManPluginReceiveResult function


## -description

Reports results for the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_receive">WSMAN_PLUGIN_RECEIVE</a> plug-in call and  is used by most shell plug-ins that return results.  After  all of the data is received,
the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> method must be called.

## -parameters

### -param requestDetails [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags [in]

Reserved for future use. Must be set to zero.

### -param stream [in, optional]

Specifies the stream that the data is associated with. Any stream can be used, but the standard streams are STDIN, STDOUT, and STDERR.

### -param streamResult [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that specifies the result object that is returned to the client. The result can be in either binary or XML format.

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

Ignored in all cases except when <i>commandState</i> is either <b>WSMAN_RECEIVE_STATE_NORMAL_TERMINATION</b> or <b>WSMAN_RECEIVE_STATE_ABNORMAL_TERMINATION</b>. Each result can have separate error codes. If the command or stream has failed, the plug-in must call the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> method.