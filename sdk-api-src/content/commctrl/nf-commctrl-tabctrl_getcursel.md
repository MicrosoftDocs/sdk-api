---
UID: NF:commctrl.TabCtrl_GetCurSel
title: TabCtrl_GetCurSel macro (commctrl.h)
description: Determines the currently selected tab in a tab control. You can use this macro or send the TCM_GETCURSEL message explicitly.
helpviewer_keywords: ["TabCtrl_GetCurSel","TabCtrl_GetCurSel macro [Windows Controls]","_win32_TabCtrl_GetCurSel","_win32_TabCtrl_GetCurSel_cpp","commctrl/TabCtrl_GetCurSel","controls.TabCtrl_GetCurSel","controls._win32_TabCtrl_GetCurSel"]
old-location: controls\TabCtrl_GetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getcursel.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetCurSel, TabCtrl_GetCurSel macro [Windows Controls], _win32_TabCtrl_GetCurSel, _win32_TabCtrl_GetCurSel_cpp, commctrl/TabCtrl_GetCurSel, controls.TabCtrl_GetCurSel, controls._win32_TabCtrl_GetCurSel
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
 - TabCtrl_GetCurSel
 - commctrl/TabCtrl_GetCurSel
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
 - TabCtrl_GetCurSel
---

# TabCtrl_GetCurSel macro

## -syntax

```cpp
int TabCtrl_GetCurSel(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the index of the selected tab if successful, or -1 if no tab is selected.


## -description

Determines the currently selected tab in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-getcursel">TCM_GETCURSEL</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.
