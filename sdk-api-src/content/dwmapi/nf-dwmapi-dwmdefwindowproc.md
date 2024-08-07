---
UID: NF:dwmapi.DwmDefWindowProc
title: DwmDefWindowProc function (dwmapi.h)
description: Default window procedure for Desktop Window Manager (DWM) hit testing within the non-client area.
helpviewer_keywords: ["DwmDefWindowProc","DwmDefWindowProc function [Desktop Window Manager]","_udwm_dwmdefwindowproc","_udwm_dwmdefwindowproc_cpp","dwm.dwmdefwindowproc","dwmapi/DwmDefWindowProc","winui._udwm_dwmdefwindowproc"]
old-location: dwm\dwmdefwindowproc.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmdefwindowproc.htm
ms.date: 12/05/2018
ms.keywords: DwmDefWindowProc, DwmDefWindowProc function [Desktop Window Manager], _udwm_dwmdefwindowproc, _udwm_dwmdefwindowproc_cpp, dwm.dwmdefwindowproc, dwmapi/DwmDefWindowProc, winui._udwm_dwmdefwindowproc
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
 - DwmDefWindowProc
 - dwmapi/DwmDefWindowProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
api_name:
 - DwmDefWindowProc
---

# DwmDefWindowProc function


## -description

Default window procedure for Desktop Window Manager (DWM) hit testing within the non-client area.

You also need to ensure that <b>DwmDefWindowProc</b> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave">WM_NCMOUSELEAVE</a> message. If <b>DwmDefWindowProc</b> is not called for the <b>WM_NCMOUSELEAVE</b> message, DWM does not remove the highlighting from the <b>Maximize</b>, <b>Minimize</b>, and <b>Close</b> buttons when the cursor leaves the window.

## -parameters

### -param hWnd [in]

A handle to the window procedure that received the message.

### -param msg [in]

The message.

### -param wParam [in]

Specifies additional message information. The content of this parameter depends on the value of the <i>msg</i> parameter.

### -param lParam [in]

Specifies additional message information. The content of this parameter depends on the value of the <i>msg</i> parameter.

### -param plResult [out]

A pointer to an <b>LRESULT</b> value that, when this method returns successfully,receives the result of the hit test.

## -returns

<b>TRUE</b> if <b>DwmDefWindowProc</b> handled the message; otherwise, <b>FALSE</b>.

## -remarks

When creating custom frames that include the standard caption buttons, <a href="/windows/desktop/inputdev/wm-nchittest">WM_NCHITTEST</a> and other non-client hit test messages should first be passed to the <b>DwmDefWindowProc</b> function. This enables the DWM to provide hit testing for the captions buttons. If <b>DwmDefWindowProc</b> does not handle the non-client hit test messages, further processing of these messages might be necessary.