---
UID: NF:winuser.SystemParametersInfoForDpi
title: SystemParametersInfoForDpi function (winuser.h)
description: Retrieves the value of one of the system-wide parameters, taking into account the provided DPI value.
helpviewer_keywords: ["SystemParametersInfoForDpi","SystemParametersInfoForDpi function [High DPI]","hidpi.systemparametersinfofordpi","winuser/SystemParametersInfoForDpi"]
old-location: hidpi\systemparametersinfofordpi.htm
tech.root: hidpi
ms.assetid: BA460A5B-5356-43A5-B232-03E6E72D15A2
ms.date: 12/05/2018
ms.keywords: SystemParametersInfoForDpi, SystemParametersInfoForDpi function [High DPI], hidpi.systemparametersinfofordpi, winuser/SystemParametersInfoForDpi
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SystemParametersInfoForDpi
 - winuser/SystemParametersInfoForDpi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SystemParametersInfoForDpi
---

# SystemParametersInfoForDpi function


## -description

Retrieves the value of one of the system-wide parameters, taking into account the provided DPI value.

## -parameters

### -param uiAction [in]

The system-wide parameter to be retrieved. This function is only intended for use with <b>SPI_GETICONTITLELOGFONT</b>, <b>SPI_GETICONMETRICS</b>, or <b>SPI_GETNONCLIENTMETRICS</b>. See <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> for more information on these values.

### -param uiParam [in]

A parameter whose usage and format depends on the system parameter being queried. For more information about system-wide parameters, see the <i>uiAction</i> parameter. If not otherwise indicated, you must specify zero for this parameter.

### -param pvParam [in, out]

A parameter whose usage and format depends on the system parameter being queried. For more information about system-wide parameters, see the <i>uiAction</i> parameter. If not otherwise indicated, you must specify <b>NULL</b> for this parameter. For information on the <b>PVOID</b> datatype, see <a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>.

### -param fWinIni [in]

Has no effect for with this API. This parameter only has an effect if you're setting parameter.

### -param dpi [in]

The DPI to use for scaling the metric.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function returns a similar result as <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>, but scales it according to an arbitrary DPI you provide (if appropriate). It only scales with the following possible values for <i>uiAction</i>: <b>SPI_GETICONTITLELOGFONT</b>, <b>SPI_GETICONMETRICS</b>, <b>SPI_GETNONCLIENTMETRICS</b>. Other possible <i>uiAction</i> values do not provide ForDPI behavior, and therefore this function returns 0 if called with them.

For <i>uiAction</i> values that contain strings within their associated structures, only Unicode (<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONTW</a>) strings are supported in this function.