---
UID: NF:commctrl.TabCtrl_InsertItem
title: TabCtrl_InsertItem macro (commctrl.h)
description: Inserts a new tab in a tab control. You can use this macro or send the TCM_INSERTITEM message explicitly.
helpviewer_keywords: ["TabCtrl_InsertItem","TabCtrl_InsertItem macro [Windows Controls]","_win32_TabCtrl_InsertItem","_win32_TabCtrl_InsertItem_cpp","commctrl/TabCtrl_InsertItem","controls.TabCtrl_InsertItem","controls._win32_TabCtrl_InsertItem"]
old-location: controls\TabCtrl_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_insertitem.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_InsertItem, TabCtrl_InsertItem macro [Windows Controls], _win32_TabCtrl_InsertItem, _win32_TabCtrl_InsertItem_cpp, commctrl/TabCtrl_InsertItem, controls.TabCtrl_InsertItem, controls._win32_TabCtrl_InsertItem
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
 - TabCtrl_InsertItem
 - commctrl/TabCtrl_InsertItem
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
 - TabCtrl_InsertItem
---

# TabCtrl_InsertItem macro

## -syntax

```cpp
int TabCtrl_InsertItem(
         HWND     hwnd,
         int      iItem,
   const LPTCITEM pitem
);
```

## -returns

Type: **int**

Returns the index of the new tab if successful, or -1 otherwise.


## -description

Inserts a new tab in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-insertitem">TCM_INSERTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param iItem

Type: <b>int</b>

Index of the new tab.

### -param pitem

Type: <b>const LPTCITEM</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-tcitema">TCITEM</a> structure that specifies the attributes of the tab. The <b>dwState</b> and <b>dwStateMask</b> members of this structure are ignored by this message.
