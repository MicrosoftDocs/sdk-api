---
UID: NF:commctrl.ListView_DeleteAllItems
title: ListView_DeleteAllItems macro (commctrl.h)
description: Removes all items from a list-view control. You can use this macro or send the LVM_DELETEALLITEMS message explicitly.
helpviewer_keywords: ["ListView_DeleteAllItems","ListView_DeleteAllItems macro [Windows Controls]","_win32_ListView_DeleteAllItems","_win32_ListView_DeleteAllItems_cpp","commctrl/ListView_DeleteAllItems","controls.ListView_DeleteAllItems","controls._win32_ListView_DeleteAllItems"]
old-location: controls\ListView_DeleteAllItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_deleteallitems.htm
ms.date: 10/21/2024
ms.keywords: ListView_DeleteAllItems, ListView_DeleteAllItems macro [Windows Controls], _win32_ListView_DeleteAllItems, _win32_ListView_DeleteAllItems_cpp, commctrl/ListView_DeleteAllItems, controls.ListView_DeleteAllItems, controls._win32_ListView_DeleteAllItems
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
 - ListView_DeleteAllItems
 - commctrl/ListView_DeleteAllItems
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
 - ListView_DeleteAllItems
---

# ListView_DeleteAllItems macro

## -syntax

```cpp
BOOL ListView_DeleteAllItems(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Removes all items from a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-deleteallitems">LVM_DELETEALLITEMS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

When a list-view control receives the <a href="/windows/desktop/Controls/lvm-deleteallitems">LVM_DELETEALLITEMS</a> message, it sends the <a href="/windows/desktop/Controls/lvn-deleteallitems">LVN_DELETEALLITEMS</a> notification code to its parent window.
