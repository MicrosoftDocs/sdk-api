---
UID: NF:dwmapi.DwmSetPresentParameters
title: DwmSetPresentParameters function (dwmapi.h)
description: Sets the present parameters for frame composition. DwmSetPresentParameters is no longer supported. Starting with Windows 8.1, calls to DwmSetPresentParameters always return E_NOTIMPL.
helpviewer_keywords: ["DwmSetPresentParameters","DwmSetPresentParameters function [Desktop Window Manager]","_udwm_dwmsetpresentparameters","_udwm_dwmsetpresentparameters_cpp","dwm.dwmsetpresentparameters","dwmapi/DwmSetPresentParameters","winui._udwm_dwmsetpresentparameters"]
old-location: dwm\dwmsetpresentparameters.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmsetpresentparameters.htm
ms.date: 12/05/2018
ms.keywords: DwmSetPresentParameters, DwmSetPresentParameters function [Desktop Window Manager], _udwm_dwmsetpresentparameters, _udwm_dwmsetpresentparameters_cpp, dwm.dwmsetpresentparameters, dwmapi/DwmSetPresentParameters, winui._udwm_dwmsetpresentparameters
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
 - DwmSetPresentParameters
 - dwmapi/DwmSetPresentParameters
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
 - DwmSetPresentParameters
---

# DwmSetPresentParameters function


## -description

Sets the present parameters for frame composition.
        
            

<b>DwmSetPresentParameters</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmSetPresentParameters</b> always return E_NOTIMPL.

## -parameters

### -param hwnd [in]

The handle to the window where the present parameters are applied.

### -param pPresentParams [in, out]

A pointer to a <a href="/windows/desktop/api/dwmapi/ns-dwmapi-dwm_present_parameters">DWM_PRESENT_PARAMETERS</a> structure that contains DWM video frame parameters for frame composition.

## -returns

This function always returns S_OK.