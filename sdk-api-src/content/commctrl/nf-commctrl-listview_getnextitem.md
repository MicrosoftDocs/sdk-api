---
UID: NF:commctrl.ListView_GetNextItem
title: ListView_GetNextItem macro (commctrl.h)
description: Searches for a list-view item that has the specified properties and bears the specified relationship to a specified item. You can use this macro or send the LVM_GETNEXTITEM message explicitly.
helpviewer_keywords: ["ListView_GetNextItem","ListView_GetNextItem macro [Windows Controls]","_win32_ListView_GetNextItem","_win32_ListView_GetNextItem_cpp","commctrl/ListView_GetNextItem","controls.ListView_GetNextItem","controls._win32_ListView_GetNextItem"]
old-location: controls\ListView_GetNextItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getnextitem.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetNextItem, ListView_GetNextItem macro [Windows Controls], _win32_ListView_GetNextItem, _win32_ListView_GetNextItem_cpp, commctrl/ListView_GetNextItem, controls.ListView_GetNextItem, controls._win32_ListView_GetNextItem
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
 - ListView_GetNextItem
 - commctrl/ListView_GetNextItem
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
 - ListView_GetNextItem
---

# ListView_GetNextItem macro

## -syntax

```cpp
int ListView_GetNextItem(
   HWND hwnd,
   int  i,
   UINT flags
);
```

## -returns

Type: **int**

Returns the index of the next item if successful, or -1 otherwise.


## -description

Searches for a list-view item that has the specified properties and bears the specified relationship to a specified item. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getnextitem">LVM_GETNEXTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the item with which to begin the search, or -1 to find the first item that matches the specified flags. The specified item itself is excluded from the search.

### -param flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The geometric relation of the requested item to the specified item and, if specified, the state of the requested item. For a list of possible values, see the description of the 
					<i>lParam</i> parameter in the <a href="/windows/desktop/Controls/lvm-getnextitem">LVM_GETNEXTITEM</a> message. If an item does not have all of the specified state flags set, the search continues with the next item.
