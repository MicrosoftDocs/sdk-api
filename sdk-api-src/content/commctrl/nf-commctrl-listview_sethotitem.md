---
UID: NF:commctrl.ListView_SetHotItem
title: ListView_SetHotItem macro (commctrl.h)
description: Sets the hot item in a list-view control. You can use this macro or send the LVM_SETHOTITEM message explicitly.
helpviewer_keywords: ["ListView_SetHotItem","ListView_SetHotItem macro [Windows Controls]","_win32_ListView_SetHotItem","_win32_ListView_SetHotItem_cpp","commctrl/ListView_SetHotItem","controls.ListView_SetHotItem","controls._win32_ListView_SetHotItem"]
old-location: controls\ListView_SetHotItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sethotitem.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetHotItem, ListView_SetHotItem macro [Windows Controls], _win32_ListView_SetHotItem, _win32_ListView_SetHotItem_cpp, commctrl/ListView_SetHotItem, controls.ListView_SetHotItem, controls._win32_ListView_SetHotItem
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
 - ListView_SetHotItem
 - commctrl/ListView_SetHotItem
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
 - ListView_SetHotItem
---

# ListView_SetHotItem macro

## -syntax

```cpp
INT ListView_SetHotItem(
   HWND hwnd,
   INT  i
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns the index of the item that was previously hot.


## -description

Sets the hot item in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-sethotitem">LVM_SETHOTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

### -param i

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The zero-based index of the item to be set as the hot item.
