---
UID: NF:commctrl.ListView_EnsureVisible
title: ListView_EnsureVisible macro (commctrl.h)
description: Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary. You can use this macro or send the LVM_ENSUREVISIBLE message explicitly.
helpviewer_keywords: ["ListView_EnsureVisible","ListView_EnsureVisible macro [Windows Controls]","_win32_ListView_EnsureVisible","_win32_ListView_EnsureVisible_cpp","commctrl/ListView_EnsureVisible","controls.ListView_EnsureVisible","controls._win32_ListView_EnsureVisible"]
old-location: controls\ListView_EnsureVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_ensurevisible.htm
ms.date: 10/21/2024
ms.keywords: ListView_EnsureVisible, ListView_EnsureVisible macro [Windows Controls], _win32_ListView_EnsureVisible, _win32_ListView_EnsureVisible_cpp, commctrl/ListView_EnsureVisible, controls.ListView_EnsureVisible, controls._win32_ListView_EnsureVisible
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
 - ListView_EnsureVisible
 - commctrl/ListView_EnsureVisible
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
 - ListView_EnsureVisible
---

# ListView_EnsureVisible macro

## -syntax

```cpp
BOOL ListView_EnsureVisible(
   HWND hwndLV,
   int  i,
   BOOL fPartialOK
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-ensurevisible">LVM_ENSUREVISIBLE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the list-view item.

### -param fPartialOK

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A value specifying whether the item must be entirely visible. If this parameter is <b>TRUE</b>, no scrolling occurs if the item is at least partially visible.
