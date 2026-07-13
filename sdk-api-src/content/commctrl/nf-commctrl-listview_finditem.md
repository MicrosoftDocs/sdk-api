---
UID: NF:commctrl.ListView_FindItem
title: ListView_FindItem macro (commctrl.h)
description: Searches for a list-view item with the specified characteristics. You can use this macro or send the LVM_FINDITEM message explicitly.
helpviewer_keywords: ["ListView_FindItem","ListView_FindItem macro [Windows Controls]","_win32_ListView_FindItem","_win32_ListView_FindItem_cpp","commctrl/ListView_FindItem","controls.ListView_FindItem","controls._win32_ListView_FindItem"]
old-location: controls\ListView_FindItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_finditem.htm
ms.date: 10/21/2024
ms.keywords: ListView_FindItem, ListView_FindItem macro [Windows Controls], _win32_ListView_FindItem, _win32_ListView_FindItem_cpp, commctrl/ListView_FindItem, controls.ListView_FindItem, controls._win32_ListView_FindItem
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
 - ListView_FindItem
 - commctrl/ListView_FindItem
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
 - ListView_FindItem
---

# ListView_FindItem macro

## -syntax

```cpp
int ListView_FindItem(
         HWND         hwnd,
         int          iStart,
   const LPLVFINDINFO plvfi
);
```

## -returns

Type: **int**

Returns the index of the item if successful, or -1 otherwise.


## -description

Searches for a list-view item with the specified characteristics. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-finditem">LVM_FINDITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iStart

Type: <b>int</b>

The index of the item after which to begin the search, or -1 to start from the beginning.

### -param plvfi

Type: <b>const LPLVFINDINFO</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvfindinfoa">LVFINDINFO</a> structure that contains information about what to search for.
