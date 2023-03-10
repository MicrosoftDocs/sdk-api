---
UID: NF:commctrl.InitCommonControls
title: InitCommonControls function (commctrl.h)
description: Registers and initializes certain common control window classes. This function is obsolete. New applications should use the InitCommonControlsEx function.
helpviewer_keywords: ["InitCommonControls","InitCommonControls function [Windows Controls]","_win32_InitCommonControls","_win32_InitCommonControls_cpp","commctrl/InitCommonControls","controls.InitCommonControls","controls._win32_InitCommonControls"]
old-location: controls\InitCommonControls.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\initcommoncontrols.htm
ms.date: 12/05/2018
ms.keywords: InitCommonControls, InitCommonControls function [Windows Controls], _win32_InitCommonControls, _win32_InitCommonControls_cpp, commctrl/InitCommonControls, controls.InitCommonControls, controls._win32_InitCommonControls
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
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitCommonControls
 - commctrl/InitCommonControls
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
 - InitCommonControls
req.apiset: ext-ms-win-shell-comctl32-init-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# InitCommonControls function


## -description

Registers and initializes certain common control window classes. This function is obsolete. New applications should use the <a href="/windows/desktop/api/commctrl/nf-commctrl-initcommoncontrolsex">InitCommonControlsEx</a> function.



## -remarks

Under Comctl32.dll version 5.x, only Windows 95 classes (ICC_WIN95_CLASSES) can be registered through <b>InitCommonControls</b>. Programs which require additional common control classes must use the <a href="/windows/desktop/api/commctrl/nf-commctrl-initcommoncontrolsex">InitCommonControlsEx</a> function.

Under Comctl32.dll version 6.0 and later, <b>InitCommonControls</b> does nothing. Applications must explicitly register all common controls through <a href="/windows/desktop/api/commctrl/nf-commctrl-initcommoncontrolsex">InitCommonControlsEx</a>.
