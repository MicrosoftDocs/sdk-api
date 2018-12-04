---
UID: NF:wsman.WSManPluginReportContext
title: WSManPluginReportContext function
author: windows-sdk-content
description: Reports shell and command context back to the Windows Remote Management (WinRM) infrastructure so that further operations can be performed against the shell and/or command.
old-location: winrm\wsmanpluginreportcontext.htm
tech.root: winrm
ms.assetid: 8bdfeabf-1028-4ddb-8953-455bbc2a1a1e
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: WSManPluginReportContext, WSManPluginReportContext function [Windows Remote Management], winrm.wsmanpluginreportcontext, wsman/WSManPluginReportContext
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
 - WSManPluginReportContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# WSManPluginReportContext function


## -description


Reports shell and command context back to the Windows Remote Management (WinRM) infrastructure so that further operations can be performed against the shell and/or command. This method is called only for <a href="https://msdn.microsoft.com/3016612a-ce99-405b-afae-200bcad9ed20">WSManPluginShell</a> and <a href="https://msdn.microsoft.com/df4b4e7b-cf30-4eb0-b646-49b17c883a16">WSManPluginCommand</a> plug-in entry points.


## -parameters




### -param requestDetails [in]

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags [in]

Reserved for future use. Must be set to zero.


### -param context [in]

Defines the value to pass into all future shell and command operations. Represents either the shell or the command. This value should be unique for all shells, and it should also be unique for all commands associated with a shell.


## -returns



The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code.  If this method returns an error, the plug-in should shut down the current operation and call the <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a> method.



