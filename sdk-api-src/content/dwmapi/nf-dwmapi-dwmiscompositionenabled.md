---
UID: NF:dwmapi.DwmIsCompositionEnabled
title: DwmIsCompositionEnabled function (dwmapi.h)
description: Obtains a value that indicates whether Desktop Window Manager (DWM) composition is enabled. Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the WM_DWMCOMPOSITIONCHANGED notification.
helpviewer_keywords: ["DwmIsCompositionEnabled","DwmIsCompositionEnabled function [Desktop Window Manager]","_udwm_dwmiscompositionenabled","_udwm_dwmiscompositionenabled_cpp","dwm.dwmiscompositionenabled","dwmapi/DwmIsCompositionEnabled","winui._udwm_dwmiscompositionenabled"]
old-location: dwm\dwmiscompositionenabled.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmiscompositionenabled.htm
ms.date: 12/05/2018
ms.keywords: DwmIsCompositionEnabled, DwmIsCompositionEnabled function [Desktop Window Manager], _udwm_dwmiscompositionenabled, _udwm_dwmiscompositionenabled_cpp, dwm.dwmiscompositionenabled, dwmapi/DwmIsCompositionEnabled, winui._udwm_dwmiscompositionenabled
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
 - DwmIsCompositionEnabled
 - dwmapi/DwmIsCompositionEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - API-MS-Win-dwmapi-l1-1-0.dll
 - Ext-Ms-Win-DwmAPI-Ext-L1-1-0.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
api_name:
 - DwmIsCompositionEnabled
---

# DwmIsCompositionEnabled function


## -description

Obtains a value that indicates whether Desktop Window Manager (DWM) composition is enabled. Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="/windows/desktop/dwm/wm-dwmcompositionchanged">WM_DWMCOMPOSITIONCHANGED</a> notification.

## -parameters

### -param pfEnabled [out]

A pointer to a value that, when this function returns successfully, receives <b>TRUE</b> if DWM composition is enabled; otherwise, <b>FALSE</b>.

                        

<div class="alert"><b>Note</b>  As of Windows 8, DWM composition is always enabled. If an app declares Windows 8 compatibility in their manifest, this function will receive a value of <b>TRUE</b> through <i>pfEnabled</i>. If no such manifest entry is found, Windows 8 compatibility is not assumed and this function receives a value of <b>FALSE</b> through <i>pfEnabled</i>. This is done so that older programs that interpret a value of <b>TRUE</b> to imply that high contrast mode is off can continue to make the correct decisions about rendering their images. (Note that this is a bad practice—you should use the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function with the <b>SPI_GETHIGHCONTRAST</b> flag to determine the state of high contrast mode.)</div>
<div> </div>
For more information, see <a href="/windows/win32/controls/supporting-high-contrast-themes">Supporting High Contrast Themes</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.