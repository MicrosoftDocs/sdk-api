---
UID: NF:commctrl.ListView_GetHotItem
title: ListView_GetHotItem macro (commctrl.h)
description: Gets the index of the hot item. You can use this macro or send the LVM_GETHOTITEM message explicitly.
helpviewer_keywords: ["ListView_GetHotItem","ListView_GetHotItem macro [Windows Controls]","_win32_ListView_GetHotItem","_win32_ListView_GetHotItem_cpp","commctrl/ListView_GetHotItem","controls.ListView_GetHotItem","controls._win32_ListView_GetHotItem"]
old-location: controls\ListView_GetHotItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gethotitem.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetHotItem, ListView_GetHotItem macro [Windows Controls], _win32_ListView_GetHotItem, _win32_ListView_GetHotItem_cpp, commctrl/ListView_GetHotItem, controls.ListView_GetHotItem, controls._win32_ListView_GetHotItem
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
 - ListView_GetHotItem
 - commctrl/ListView_GetHotItem
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
 - ListView_GetHotItem
---

# ListView_GetHotItem macro

## -syntax

```cpp
INT ListView_GetHotItem(
   HWND hwnd
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns the index of the item that is currently hot.


## -description

Gets the index of the hot item. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gethotitem">LVM_GETHOTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.
