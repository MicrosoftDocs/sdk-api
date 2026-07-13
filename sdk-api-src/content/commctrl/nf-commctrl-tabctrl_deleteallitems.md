---
UID: NF:commctrl.TabCtrl_DeleteAllItems
title: TabCtrl_DeleteAllItems macro (commctrl.h)
description: Removes all items from a tab control. You can use this macro or send the TCM_DELETEALLITEMS message explicitly.
helpviewer_keywords: ["TabCtrl_DeleteAllItems","TabCtrl_DeleteAllItems macro [Windows Controls]","_win32_TabCtrl_DeleteAllItems","_win32_TabCtrl_DeleteAllItems_cpp","commctrl/TabCtrl_DeleteAllItems","controls.TabCtrl_DeleteAllItems","controls._win32_TabCtrl_DeleteAllItems"]
old-location: controls\TabCtrl_DeleteAllItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_deleteallitems.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_DeleteAllItems, TabCtrl_DeleteAllItems macro [Windows Controls], _win32_TabCtrl_DeleteAllItems, _win32_TabCtrl_DeleteAllItems_cpp, commctrl/TabCtrl_DeleteAllItems, controls.TabCtrl_DeleteAllItems, controls._win32_TabCtrl_DeleteAllItems
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
 - TabCtrl_DeleteAllItems
 - commctrl/TabCtrl_DeleteAllItems
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
 - TabCtrl_DeleteAllItems
---

# TabCtrl_DeleteAllItems macro

## -syntax

```cpp
BOOL TabCtrl_DeleteAllItems(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Removes all items from a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-deleteallitems">TCM_DELETEALLITEMS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.
