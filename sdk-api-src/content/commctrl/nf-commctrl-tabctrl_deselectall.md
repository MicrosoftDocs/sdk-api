---
UID: NF:commctrl.TabCtrl_DeselectAll
title: TabCtrl_DeselectAll macro (commctrl.h)
description: Resets items in a tab control, clearing any that were set to the TCIS_BUTTONPRESSED state. You can use this macro or send the TCM_DESELECTALL message explicitly.
helpviewer_keywords: ["TabCtrl_DeselectAll","TabCtrl_DeselectAll macro [Windows Controls]","_win32_TabCtrl_DeselectAll","_win32_TabCtrl_DeselectAll_cpp","commctrl/TabCtrl_DeselectAll","controls.TabCtrl_DeselectAll","controls._win32_TabCtrl_DeselectAll"]
old-location: controls\TabCtrl_DeselectAll.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_deselectall.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_DeselectAll, TabCtrl_DeselectAll macro [Windows Controls], _win32_TabCtrl_DeselectAll, _win32_TabCtrl_DeselectAll_cpp, commctrl/TabCtrl_DeselectAll, controls.TabCtrl_DeselectAll, controls._win32_TabCtrl_DeselectAll
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
 - TabCtrl_DeselectAll
 - commctrl/TabCtrl_DeselectAll
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
 - TabCtrl_DeselectAll
---

# TabCtrl_DeselectAll macro

## -syntax

```cpp
VOID TabCtrl_DeselectAll(
   HWND hwnd,
   UINT fExcludeFocus
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

The return value is not used.


## -description

Resets items in a tab control, clearing any that were set to the <a href="/windows/desktop/Controls/tab-control-item-states">TCIS_BUTTONPRESSED</a> state. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-deselectall">TCM_DESELECTALL</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param fExcludeFocus

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flag value that specifies the scope of the item deselection. If this parameter is set to <b>FALSE</b>, all tab items will be reset. If it is set to <b>TRUE</b>, all but the currently selected tab item will be reset.

## -remarks

This message is only meaningful if the <a href="/windows/desktop/Controls/tab-control-styles">TCS_BUTTONS</a> style flag has been set.
