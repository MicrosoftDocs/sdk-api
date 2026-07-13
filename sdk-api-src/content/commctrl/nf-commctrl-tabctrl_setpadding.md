---
UID: NF:commctrl.TabCtrl_SetPadding
title: TabCtrl_SetPadding macro (commctrl.h)
description: Sets the amount of space (padding) around each tab's icon and label in a tab control. You can use this macro or send the TCM_SETPADDING message explicitly.
helpviewer_keywords: ["TabCtrl_SetPadding","TabCtrl_SetPadding macro [Windows Controls]","_win32_TabCtrl_SetPadding","_win32_TabCtrl_SetPadding_cpp","commctrl/TabCtrl_SetPadding","controls.TabCtrl_SetPadding","controls._win32_TabCtrl_SetPadding"]
old-location: controls\TabCtrl_SetPadding.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setpadding.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_SetPadding, TabCtrl_SetPadding macro [Windows Controls], _win32_TabCtrl_SetPadding, _win32_TabCtrl_SetPadding_cpp, commctrl/TabCtrl_SetPadding, controls.TabCtrl_SetPadding, controls._win32_TabCtrl_SetPadding
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
 - TabCtrl_SetPadding
 - commctrl/TabCtrl_SetPadding
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
 - TabCtrl_SetPadding
---

# TabCtrl_SetPadding macro

## -syntax

```cpp
void TabCtrl_SetPadding(
   HWND hwnd,
   int  cx,
   int  cy
);
```


## -description

Sets the amount of space (padding) around each tab's icon and label in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-setpadding">TCM_SETPADDING</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param cx

Type: <b>int</b>

Amount of horizontal padding, in pixels.

### -param cy

Type: <b>int</b>

Amount of vertical padding, in pixels.
