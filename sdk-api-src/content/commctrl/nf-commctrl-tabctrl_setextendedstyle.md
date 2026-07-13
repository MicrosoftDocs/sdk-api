---
UID: NF:commctrl.TabCtrl_SetExtendedStyle
title: TabCtrl_SetExtendedStyle macro (commctrl.h)
description: Sets the extended styles that the tab control will use. You can use this macro or send the TCM_SETEXTENDEDSTYLE message explicitly.
helpviewer_keywords: ["TabCtrl_SetExtendedStyle","TabCtrl_SetExtendedStyle macro [Windows Controls]","_win32_TabCtrl_SetExtendedStyle","_win32_TabCtrl_SetExtendedStyle_cpp","commctrl/TabCtrl_SetExtendedStyle","controls.TabCtrl_SetExtendedStyle","controls._win32_TabCtrl_SetExtendedStyle"]
old-location: controls\TabCtrl_SetExtendedStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setextendedstyle.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_SetExtendedStyle, TabCtrl_SetExtendedStyle macro [Windows Controls], _win32_TabCtrl_SetExtendedStyle, _win32_TabCtrl_SetExtendedStyle_cpp, commctrl/TabCtrl_SetExtendedStyle, controls.TabCtrl_SetExtendedStyle, controls._win32_TabCtrl_SetExtendedStyle
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
 - TabCtrl_SetExtendedStyle
 - commctrl/TabCtrl_SetExtendedStyle
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
 - TabCtrl_SetExtendedStyle
---

# TabCtrl_SetExtendedStyle macro

## -syntax

```cpp
DWORD TabCtrl_SetExtendedStyle(
   HWND  hwnd,
   DWORD dw
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that contains the previous tab control extended styles.


## -description

Sets the extended styles that the tab control will use. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-setextendedstyle">TCM_SETEXTENDEDSTYLE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param dw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Value that contains the new tab control extended styles. This value is a combination of tab control <a href="/windows/desktop/Controls/tab-control-extended-styles">extended styles</a>.
