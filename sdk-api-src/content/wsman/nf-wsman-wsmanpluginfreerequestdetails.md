---
UID: NF:wsman.WSManPluginFreeRequestDetails
title: WSManPluginFreeRequestDetails function (wsman.h)
description: Releases memory that is allocated for the WSMAN_PLUGIN_REQUEST structure, which is passed into operation plug-in entry points.
helpviewer_keywords: ["WSManPluginFreeRequestDetails","WSManPluginFreeRequestDetails function [Windows Remote Management]","winrm.wsmanpluginfreerequestdetails","wsman/WSManPluginFreeRequestDetails"]
old-location: winrm\wsmanpluginfreerequestdetails.htm
tech.root: winrm
ms.assetid: 43716391-536c-49ae-9266-a8ae72621a0b
ms.date: 12/05/2018
ms.keywords: WSManPluginFreeRequestDetails, WSManPluginFreeRequestDetails function [Windows Remote Management], winrm.wsmanpluginfreerequestdetails, wsman/WSManPluginFreeRequestDetails
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
 - WSManPluginFreeRequestDetails
 - wsman/WSManPluginFreeRequestDetails
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
 - WSManPluginFreeRequestDetails
---

# WSManPluginFreeRequestDetails function


## -description

Releases memory that is allocated for the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure, which is passed into operation plug-in entry points. This method is optional and can be called at any point after a plug-in entry point is called and before the entry point calls the  <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginoperationcomplete">WSManPluginOperationComplete</a> method. After this method is called, the memory will be released and the plug-in will be unable to access any of the parameters in the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure.

## -parameters

### -param requestDetails [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_plugin_request">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.