---
UID: NF:commctrl.ListView_GetItemSpacing
title: ListView_GetItemSpacing macro (commctrl.h)
description: Determines the spacing between items in a list-view control. You can use this macro or send the LVM_GETITEMSPACING message explicitly.
helpviewer_keywords: ["ListView_GetItemSpacing","ListView_GetItemSpacing macro [Windows Controls]","_win32_ListView_GetItemSpacing","_win32_ListView_GetItemSpacing_cpp","commctrl/ListView_GetItemSpacing","controls.ListView_GetItemSpacing","controls._win32_ListView_GetItemSpacing"]
old-location: controls\ListView_GetItemSpacing.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemspacing.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetItemSpacing, ListView_GetItemSpacing macro [Windows Controls], _win32_ListView_GetItemSpacing, _win32_ListView_GetItemSpacing_cpp, commctrl/ListView_GetItemSpacing, controls.ListView_GetItemSpacing, controls._win32_ListView_GetItemSpacing
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
 - ListView_GetItemSpacing
 - commctrl/ListView_GetItemSpacing
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
 - ListView_GetItemSpacing
---

# ListView_GetItemSpacing macro

## -syntax

```cpp
DWORD ListView_GetItemSpacing(
   HWND hwndLV,
   BOOL fSmall
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the amount of spacing between items. The horizontal spacing is contained in the <b>LOWORD</b> and the vertical spacing is contained in the <b>HIWORD</b>.


## -description

Determines the spacing between items in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getitemspacing">LVM_GETITEMSPACING</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param fSmall

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A view for which to retrieve the item spacing. This parameter is <b>TRUE</b> for small icon view, or <b>FALSE</b> for icon view.
