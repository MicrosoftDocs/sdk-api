---
UID: NF:commctrl.TabCtrl_DeleteItem
title: TabCtrl_DeleteItem macro (commctrl.h)
description: Removes an item from a tab control. You can use this macro or send the TCM_DELETEITEM message explicitly.
helpviewer_keywords: ["TabCtrl_DeleteItem","TabCtrl_DeleteItem macro [Windows Controls]","_win32_TabCtrl_DeleteItem","_win32_TabCtrl_DeleteItem_cpp","commctrl/TabCtrl_DeleteItem","controls.TabCtrl_DeleteItem","controls._win32_TabCtrl_DeleteItem"]
old-location: controls\TabCtrl_DeleteItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_deleteitem.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_DeleteItem, TabCtrl_DeleteItem macro [Windows Controls], _win32_TabCtrl_DeleteItem, _win32_TabCtrl_DeleteItem_cpp, commctrl/TabCtrl_DeleteItem, controls.TabCtrl_DeleteItem, controls._win32_TabCtrl_DeleteItem
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
 - TabCtrl_DeleteItem
 - commctrl/TabCtrl_DeleteItem
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
 - TabCtrl_DeleteItem
---

# TabCtrl_DeleteItem macro

## -syntax

```cpp
BOOL TabCtrl_DeleteItem(
   HWND hwnd,
   int  i
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Removes an item from a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-deleteitem">TCM_DELETEITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param i

Type: <b>int</b>

Index of the item to delete.
