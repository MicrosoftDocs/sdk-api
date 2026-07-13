---
UID: NF:commctrl.TabCtrl_SetCurSel
title: TabCtrl_SetCurSel macro (commctrl.h)
description: Selects a tab in a tab control. You can use this macro or send the TCM_SETCURSEL message explicitly.
helpviewer_keywords: ["TabCtrl_SetCurSel","TabCtrl_SetCurSel macro [Windows Controls]","_win32_TabCtrl_SetCurSel","_win32_TabCtrl_SetCurSel_cpp","commctrl/TabCtrl_SetCurSel","controls.TabCtrl_SetCurSel","controls._win32_TabCtrl_SetCurSel"]
old-location: controls\TabCtrl_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setcursel.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_SetCurSel, TabCtrl_SetCurSel macro [Windows Controls], _win32_TabCtrl_SetCurSel, _win32_TabCtrl_SetCurSel_cpp, commctrl/TabCtrl_SetCurSel, controls.TabCtrl_SetCurSel, controls._win32_TabCtrl_SetCurSel
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TabCtrl_SetCurSel
 - commctrl/TabCtrl_SetCurSel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TabCtrl_SetCurSel
---

# TabCtrl_SetCurSel macro

## -syntax

```cpp
int TabCtrl_SetCurSel(
   HWND hwnd,
   int  i
);
```

## -returns

Type: **int**

Returns the index of the previously selected tab if successful, or -1 otherwise.


## -description

Selects a tab in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-setcursel">TCM_SETCURSEL</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param i

Type: <b>int</b>

Index of the tab to select.

## -remarks

A tab control does not send a <a href="/windows/desktop/Controls/tcn-selchanging">TCN_SELCHANGING</a> or <a href="/windows/desktop/Controls/tcn-selchange">TCN_SELCHANGE</a> notification code when a tab is selected using the <a href="/windows/desktop/Controls/tcm-setcursel">TCM_SETCURSEL</a> message.
