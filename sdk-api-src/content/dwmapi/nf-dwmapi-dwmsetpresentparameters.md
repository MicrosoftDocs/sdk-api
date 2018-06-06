---
UID: NF:dwmapi.DwmSetPresentParameters
title: DwmSetPresentParameters function
author: windows-sdk-content
description: Sets the present parameters for frame composition. DwmSetPresentParameters is no longer supported. Starting with Windows 8.1, calls to DwmSetPresentParameters always return E_NOTIMPL.
old-location: dwm\dwmsetpresentparameters.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmsetpresentparameters.htm
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: DwmSetPresentParameters, DwmSetPresentParameters function [Desktop Window Manager], _udwm_dwmsetpresentparameters, _udwm_dwmsetpresentparameters_cpp, dwm.dwmsetpresentparameters, dwmapi/DwmSetPresentParameters, winui._udwm_dwmsetpresentparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmSetPresentParameters
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmSetPresentParameters function


## -description


Sets the present parameters for frame composition.
        
            

<b>DwmSetPresentParameters</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmSetPresentParameters</b> always return E_NOTIMPL.


## -parameters




### -param hwnd

The handle to the window where the present parameters are applied.


### -param pPresentParams [in, out]

A pointer to a <a href="https://msdn.microsoft.com/9fa736e7-9816-45e7-a864-da88403369b9">DWM_PRESENT_PARAMETERS</a> structure that contains DWM video frame parameters for frame composition.


## -returns



This function always returns S_OK.



