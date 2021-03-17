---
UID: NF:wsman.WSManPluginOperationComplete
title: WSManPluginOperationComplete function (wsman.h)
description: Reports the completion of an operation by all operation entry points except for the WSManPluginStartup and WSManPluginShutdown methods.
helpviewer_keywords: ["WSManPluginOperationComplete","WSManPluginOperationComplete function [Windows Remote Management]","winrm.wsmanpluginoperationcomplete","wsman/WSManPluginOperationComplete"]
old-location: winrm\wsmanpluginoperationcomplete.htm
tech.root: winrm
ms.assetid: 6cb47762-edfc-48d7-88ec-d62056ea1751
ms.date: 12/05/2018
ms.keywords: WSManPluginOperationComplete, WSManPluginOperationComplete function [Windows Remote Management], winrm.wsmanpluginoperationcomplete, wsman/WSManPluginOperationComplete
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManPluginOperationComplete
 - wsman/WSManPluginOperationComplete
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
 - WSManPluginOperationComplete
---

# WSManPluginOperationComplete function


## -description

Reports the completion of an operation by all operation entry points except for the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a> and <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_shutdown">WSManPluginShutdown</a> methods.

## -parameters

### -param requestDetails [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags [in]

Reserved for future use. Must be zero.

### -param errorCode [in]

Reports any failure in the operation. If this parameter is not <b>NO_ERROR</b>, any result data that has not been sent will be discarded and the error will be sent.

### -param extendedInformation [in, optional]

Specifies an XML document that contains any extra error information that needs to be reported to the client. This parameter is ignored if <i>errorCode</i> is <b>NO_ERROR</b>. The user interface language of the thread should be used for localization.

## -returns

The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code. If the operation is unsuccessful, the plug-in must stop the current operation and clean up any data associated with this operation. The <i>requestDetails</i> structure is not valid if an error is received and must not be passed to any other WinRM (WinRM) method.

## -remarks

The <b>WSManPluginOperationComplete</b> function is used to report the completion of the 
data stream for <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_receive">WSManPluginReceive</a>.  The <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_shell">WSManPluginShell</a> and <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_command">WSManPluginCommand</a> operations must also call this function when the shell and command operations are complete.