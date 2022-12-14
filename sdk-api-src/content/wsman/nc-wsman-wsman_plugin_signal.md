---
UID: NC:wsman.WSMAN_PLUGIN_SIGNAL
title: WSMAN_PLUGIN_SIGNAL (wsman.h)
description: Defines the signal callback for a plug-in.
helpviewer_keywords: ["WSMAN_PLUGIN_SIGNAL","WSMAN_PLUGIN_SIGNAL callback","WSMAN_PLUGIN_SIGNAL callback function [Windows Remote Management]","WSMAN_SIGNAL_SHELL_CODE_CTRL_BREAK","WSMAN_SIGNAL_SHELL_CODE_CTRL_C","WSMAN_SIGNAL_SHELL_CODE_TERMINATE","WSManPluginSignal","winrm.wsman_plugin_signal","wsman/WSMAN_PLUGIN_SIGNAL"]
old-location: winrm\wsman_plugin_signal.htm
tech.root: winrm
ms.assetid: 380f9d24-d315-4289-add9-ebc2a6b8ca32
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_SIGNAL, WSMAN_PLUGIN_SIGNAL callback, WSMAN_PLUGIN_SIGNAL callback function [Windows Remote Management], WSMAN_SIGNAL_SHELL_CODE_CTRL_BREAK, WSMAN_SIGNAL_SHELL_CODE_CTRL_C, WSMAN_SIGNAL_SHELL_CODE_TERMINATE, WSManPluginSignal, winrm.wsman_plugin_signal, wsman/WSMAN_PLUGIN_SIGNAL
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2, and     Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSMAN_PLUGIN_SIGNAL
 - wsman/WSMAN_PLUGIN_SIGNAL
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
 - WSMAN_PLUGIN_SIGNAL
---

# WSMAN_PLUGIN_SIGNAL callback function


## -description

Defines the signal callback for a plug-in. This function is called when an inbound signal is 
     received from a client call.

The DLL entry point name for this method must be 
    <b>WSManPluginSignal</b>.

## -parameters

### -param requestDetails [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> 
      structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags [in]

Reserved for future use. Must be zero.

### -param shellContext [in]

Specifies the context that was received when the shell was created.

### -param commandContext [in, optional]

If this request is aimed at a command and not a shell, this is the context returned from the 
      <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.

### -param code [in]

Specifies the signal that is received from the client. The following codes are common.



#### WSMAN_SIGNAL_SHELL_CODE_TERMINATE

The shell or Command Prompt window was closed. The plug-in should call the 
        <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> 
        function.



#### WSMAN_SIGNAL_SHELL_CODE_CTRL_C

The signal for CTRL+C was received, and the process was halted. The plug-in should call the 
        <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> 
        function.



#### WSMAN_SIGNAL_SHELL_CODE_CTRL_BREAK

The signal for CTRL+BREAK was received, and the process was halted. The plug-in should call the 
        <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> 
        function.

## -remarks

A signal can be received for processing a CTRL+C sequence or one of many other types of custom signals. The 
    callback is called once for each signal that is received. The plug-in determines which signals cause commands 
    and/or shells to be shut down. Because signals are shell-specific, the plug-in must initiate the shutdown by 
    calling the 
    <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> method. For 
    each call, the plug-in should call 
    <b>WSManPluginOperationComplete</b> to 
    acknowledge receipt and to allow the next signal to be received.
