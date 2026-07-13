---
UID: NF:commctrl.TabCtrl_GetToolTips
title: TabCtrl_GetToolTips macro (commctrl.h)
description: Retrieves the handle to the tooltip control associated with a tab control. You can use this macro or send the TCM_GETTOOLTIPS message explicitly.
helpviewer_keywords: ["TabCtrl_GetToolTips","TabCtrl_GetToolTips macro [Windows Controls]","_win32_TabCtrl_GetToolTips","_win32_TabCtrl_GetToolTips_cpp","commctrl/TabCtrl_GetToolTips","controls.TabCtrl_GetToolTips","controls._win32_TabCtrl_GetToolTips"]
old-location: controls\TabCtrl_GetToolTips.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_gettooltips.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetToolTips, TabCtrl_GetToolTips macro [Windows Controls], _win32_TabCtrl_GetToolTips, _win32_TabCtrl_GetToolTips_cpp, commctrl/TabCtrl_GetToolTips, controls.TabCtrl_GetToolTips, controls._win32_TabCtrl_GetToolTips
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
 - TabCtrl_GetToolTips
 - commctrl/TabCtrl_GetToolTips
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
 - TabCtrl_GetToolTips
---

# TabCtrl_GetToolTips macro

## -syntax

```cpp
HWND TabCtrl_GetToolTips(
   HWND hwnd
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the tooltip control if successful, or <b>NULL</b> otherwise.


## -description

Retrieves the handle to the tooltip control associated with a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-gettooltips">TCM_GETTOOLTIPS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

## -remarks

A tab control creates a tooltip control if it has the <a href="/windows/desktop/Controls/tab-control-styles">TCS_TOOLTIPS</a>. You can also assign a tooltip control to a tab control by using the <a href="/windows/desktop/Controls/tcm-settooltips">TCM_SETTOOLTIPS</a> message.
