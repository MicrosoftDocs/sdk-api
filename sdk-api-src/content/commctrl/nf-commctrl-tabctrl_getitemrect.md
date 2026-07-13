---
UID: NF:commctrl.TabCtrl_GetItemRect
title: TabCtrl_GetItemRect macro (commctrl.h)
description: Retrieves the bounding rectangle for a tab in a tab control. You can use this macro or send the TCM_GETITEMRECT message explicitly.
helpviewer_keywords: ["TabCtrl_GetItemRect","TabCtrl_GetItemRect macro [Windows Controls]","_win32_TabCtrl_GetItemRect","_win32_TabCtrl_GetItemRect_cpp","commctrl/TabCtrl_GetItemRect","controls.TabCtrl_GetItemRect","controls._win32_TabCtrl_GetItemRect"]
old-location: controls\TabCtrl_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getitemrect.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetItemRect, TabCtrl_GetItemRect macro [Windows Controls], _win32_TabCtrl_GetItemRect, _win32_TabCtrl_GetItemRect_cpp, commctrl/TabCtrl_GetItemRect, controls.TabCtrl_GetItemRect, controls._win32_TabCtrl_GetItemRect
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
 - TabCtrl_GetItemRect
 - commctrl/TabCtrl_GetItemRect
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
 - TabCtrl_GetItemRect
---

# TabCtrl_GetItemRect macro

## -syntax

```cpp
BOOL TabCtrl_GetItemRect(
   HWND hwnd,
   int  i,
   RECT *prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Retrieves the bounding rectangle for a tab in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-getitemrect">TCM_GETITEMRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param i

Type: <b>int</b>

Index of the tab.

### -param prc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a structure that receives the bounding rectangle of the tab, in viewport coordinates.
