---
UID: NF:wsman.WSManPluginReportContext
title: WSManPluginReportContext function (wsman.h)
description: Reports shell and command context back to the Windows Remote Management (WinRM) infrastructure so that further operations can be performed against the shell and/or command.
helpviewer_keywords: ["WSManPluginReportContext","WSManPluginReportContext function [Windows Remote Management]","winrm.wsmanpluginreportcontext","wsman/WSManPluginReportContext"]
old-location: winrm\wsmanpluginreportcontext.htm
tech.root: winrm
ms.assetid: 8bdfeabf-1028-4ddb-8953-455bbc2a1a1e
ms.date: 12/05/2018
ms.keywords: WSManPluginReportContext, WSManPluginReportContext function [Windows Remote Management], winrm.wsmanpluginreportcontext, wsman/WSManPluginReportContext
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
 - WSManPluginReportContext
 - wsman/WSManPluginReportContext
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
 - WSManPluginReportContext
---

# WSManPluginReportContext function


## -description

Reports shell and command context back to the Windows Remote Management (WinRM) infrastructure so that further operations can be performed against the shell and/or command. This method is called only for <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_shell">WSManPluginShell</a> and <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_command">WSManPluginCommand</a> plug-in entry points.

## -parameters

### -param requestDetails [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.

### -param flags [in]

Reserved for future use. Must be set to zero.

### -param context [in]

Defines the value to pass into all future shell and command operations. Represents either the shell or the command. This value should be unique for all shells, and it should also be unique for all commands associated with a shell.

## -returns

The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code.  If this method returns an error, the plug-in should shut down the current operation and call the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> method.