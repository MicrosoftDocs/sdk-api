---
UID: NF:commctrl.TabCtrl_GetExtendedStyle
title: TabCtrl_GetExtendedStyle macro (commctrl.h)
description: Retrieves the extended styles that are currently in use for the tab control. You can use this macro or send the TCM_GETEXTENDEDSTYLE message explicitly.
helpviewer_keywords: ["TabCtrl_GetExtendedStyle","TabCtrl_GetExtendedStyle macro [Windows Controls]","_win32_TabCtrl_GetExtendedStyle","_win32_TabCtrl_GetExtendedStyle_cpp","commctrl/TabCtrl_GetExtendedStyle","controls.TabCtrl_GetExtendedStyle","controls._win32_TabCtrl_GetExtendedStyle"]
old-location: controls\TabCtrl_GetExtendedStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getextendedstyle.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetExtendedStyle, TabCtrl_GetExtendedStyle macro [Windows Controls], _win32_TabCtrl_GetExtendedStyle, _win32_TabCtrl_GetExtendedStyle_cpp, commctrl/TabCtrl_GetExtendedStyle, controls.TabCtrl_GetExtendedStyle, controls._win32_TabCtrl_GetExtendedStyle
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
 - TabCtrl_GetExtendedStyle
 - commctrl/TabCtrl_GetExtendedStyle
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
 - TabCtrl_GetExtendedStyle
---

# TabCtrl_GetExtendedStyle macro

## -syntax

```cpp
DWORD TabCtrl_GetExtendedStyle(
   HWND hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that represents the extended styles currently in use for the tab control. This value is a combination of tab control extended styles.


## -description

Retrieves the extended styles that are currently in use for the tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-getextendedstyle">TCM_GETEXTENDEDSTYLE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.
