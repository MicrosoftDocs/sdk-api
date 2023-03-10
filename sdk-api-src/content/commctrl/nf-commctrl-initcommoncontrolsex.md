---
UID: NF:commctrl.InitCommonControlsEx
title: InitCommonControlsEx function (commctrl.h)
description: Ensures that the common control DLL (Comctl32.dll) is loaded, and registers specific common control classes from the DLL. An application must call this function before creating a common control.
helpviewer_keywords: ["InitCommonControlsEx","InitCommonControlsEx function [Windows Controls]","_win32_InitCommonControlsEx","_win32_InitCommonControlsEx_cpp","commctrl/InitCommonControlsEx","controls.InitCommonControlsEx","controls._win32_InitCommonControlsEx"]
old-location: controls\InitCommonControlsEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\initcommoncontrolsex.htm
ms.date: 12/05/2018
ms.keywords: InitCommonControlsEx, InitCommonControlsEx function [Windows Controls], _win32_InitCommonControlsEx, _win32_InitCommonControlsEx_cpp, commctrl/InitCommonControlsEx, controls.InitCommonControlsEx, controls._win32_InitCommonControlsEx
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.70 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitCommonControlsEx
 - commctrl/InitCommonControlsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-l1-1-0.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - InitCommonControlsEx
req.apiset: ext-ms-win-shell-comctl32-init-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# InitCommonControlsEx function


## -description

Ensures that the common control DLL (Comctl32.dll) is loaded, and registers specific common control classes from the  DLL. An application must call this function before creating a common control.

## -parameters

### -param picce [in]

Type: <b>const LPINITCOMMONCONTROLSEX</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-initcommoncontrolsex">INITCOMMONCONTROLSEX</a> structure that contains information specifying which control classes will be registered.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

The effect of each call to <b>InitCommonControlsEx</b> is cumulative. For example, if <b>InitCommonControlsEx</b> is called with the <a href="/windows/desktop/api/commctrl/ns-commctrl-initcommoncontrolsex">ICC_UPDOWN_CLASS</a> flag, then is later called with the <a href="/windows/desktop/api/commctrl/ns-commctrl-initcommoncontrolsex">ICC_HOTKEY_CLASS</a> flag, the result is that both the up-down and hot key common control classes are registered and available to the application.
