---
UID: NF:commctrl.ListView_Update
title: ListView_Update macro (commctrl.h)
description: Updates a list-view item. If the list-view control has the LVS_AUTOARRANGE style, this macro causes the list-view control to be arranged. You can use this macro or send the LVM_UPDATE message explicitly.
helpviewer_keywords: ["ListView_Update","ListView_Update macro [Windows Controls]","_win32_ListView_Update","_win32_ListView_Update_cpp","commctrl/ListView_Update","controls.ListView_Update","controls._win32_ListView_Update"]
old-location: controls\ListView_Update.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_update.htm
ms.date: 10/21/2024
ms.keywords: ListView_Update, ListView_Update macro [Windows Controls], _win32_ListView_Update, _win32_ListView_Update_cpp, commctrl/ListView_Update, controls.ListView_Update, controls._win32_ListView_Update
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
 - ListView_Update
 - commctrl/ListView_Update
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
 - ListView_Update
---

# ListView_Update macro

## -syntax

```cpp
BOOL ListView_Update(
   HWND hwndLV,
   int  i
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Updates a list-view item. If the list-view control has the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_AUTOARRANGE</a> style, this macro causes the list-view control to be arranged. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-update">LVM_UPDATE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the item to update.
