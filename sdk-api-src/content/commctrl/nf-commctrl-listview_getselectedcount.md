---
UID: NF:commctrl.ListView_GetSelectedCount
title: ListView_GetSelectedCount macro (commctrl.h)
description: Determines the number of selected items in a list-view control. You can use this macro or send the LVM_GETSELECTEDCOUNT message explicitly.
helpviewer_keywords: ["ListView_GetSelectedCount","ListView_GetSelectedCount macro [Windows Controls]","_win32_ListView_GetSelectedCount","_win32_ListView_GetSelectedCount_cpp","commctrl/ListView_GetSelectedCount","controls.ListView_GetSelectedCount","controls._win32_ListView_GetSelectedCount"]
old-location: controls\ListView_GetSelectedCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectedcount.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetSelectedCount, ListView_GetSelectedCount macro [Windows Controls], _win32_ListView_GetSelectedCount, _win32_ListView_GetSelectedCount_cpp, commctrl/ListView_GetSelectedCount, controls.ListView_GetSelectedCount, controls._win32_ListView_GetSelectedCount
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
 - ListView_GetSelectedCount
 - commctrl/ListView_GetSelectedCount
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
 - ListView_GetSelectedCount
---

# ListView_GetSelectedCount macro

## -syntax

```cpp
UINT ListView_GetSelectedCount(
   HWND hwndLV
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the number of selected items.


## -description

Determines the number of selected items in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getselectedcount">LVM_GETSELECTEDCOUNT</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
