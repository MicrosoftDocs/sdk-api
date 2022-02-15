---
UID: NF:dwmapi.DwmGetTransportAttributes
title: DwmGetTransportAttributes function (dwmapi.h)
description: Retrieves transport attributes.
helpviewer_keywords: ["DwmGetTransportAttributes","DwmGetTransportAttributes function [Desktop Window Manager]","_udwm_dwmgettransportattributes","_udwm_dwmgettransportattributes_cpp","dwm.dwmgettransportattributes","dwmapi/DwmGetTransportAttributes","winui._udwm_dwmgettransportattributes"]
old-location: dwm\dwmgettransportattributes.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmgettransportattributes.htm
ms.date: 12/05/2018
ms.keywords: DwmGetTransportAttributes, DwmGetTransportAttributes function [Desktop Window Manager], _udwm_dwmgettransportattributes, _udwm_dwmgettransportattributes_cpp, dwm.dwmgettransportattributes, dwmapi/DwmGetTransportAttributes, winui._udwm_dwmgettransportattributes
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmGetTransportAttributes
 - dwmapi/DwmGetTransportAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmGetTransportAttributes
---

# DwmGetTransportAttributes function


## -description

Retrieves transport attributes.

## -parameters

### -param pfIsRemoting [out]

A pointer to a <b>BOOL</b> value that indicates whether the transport supports remoting. <b>TRUE</b> if the transport supports remoting; otherwise, <b>FALSE</b>.

### -param pfIsConnected [out]

A pointer to a <b>BOOL</b> value that indicates whether the transport is connected. <b>TRUE</b> if the transport is connected; otherwise, <b>FALSE</b>.

### -param pDwGeneration [out]

A pointer to a <b>DWORD</b> that receives a generation value for the transport.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

