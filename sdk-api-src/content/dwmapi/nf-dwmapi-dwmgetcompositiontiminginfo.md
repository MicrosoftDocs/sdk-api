---
UID: NF:dwmapi.DwmGetCompositionTimingInfo
title: DwmGetCompositionTimingInfo function
author: windows-sdk-content
description: Retrieves the current composition timing information for a specified window.
old-location: dwm\dwmgetcompositiontiminginfo.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmgetcompositiontiminginfo.htm
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: DwmGetCompositionTimingInfo, DwmGetCompositionTimingInfo function [Desktop Window Manager], _udwm_dwmgetcompositiontiminginfo, _udwm_dwmgetcompositiontiminginfo_cpp, dwm.dwmgetcompositiontiminginfo, dwmapi/DwmGetCompositionTimingInfo, winui._udwm_dwmgetcompositiontiminginfo
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
 - API-MS-Win-dwmapi-l1-1-0.dll
 - Ext-Ms-Win-DwmAPI-Ext-L1-1-0.dll
api_name:
 - DwmGetCompositionTimingInfo
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmGetCompositionTimingInfo function


## -description


Retrieves the current composition timing information for a specified window.


## -parameters




### -param hwnd

The handle to the window for which the composition timing information should be retrieved.
        
                        

Starting with Windows 8.1, this parameter must be set to <b>NULL</b>. If this parameter is not set to <b>NULL</b>, <b>DwmGetCompositionTimingInfo</b> returns E_INVALIDARG.


### -param pTimingInfo [out]

A pointer to a <a href="https://msdn.microsoft.com/7a2bf2b0-8bf3-4702-bf48-d105d90c84c2">DWM_TIMING_INFO</a> structure that, when this function returns successfully, receives the current composition timing information for the window. The <b>cbSize</b> member of this structure must be set before this function is called.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



