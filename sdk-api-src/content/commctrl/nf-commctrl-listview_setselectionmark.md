---
UID: NF:commctrl.ListView_SetSelectionMark
title: ListView_SetSelectionMark macro (commctrl.h)
description: Sets the selection mark in a list-view control. You can use this macro or send the LVM_SETSELECTIONMARK message explicitly.
helpviewer_keywords: ["ListView_SetSelectionMark","ListView_SetSelectionMark macro [Windows Controls]","_win32_ListView_SetSelectionMark","_win32_ListView_SetSelectionMark_cpp","commctrl/ListView_SetSelectionMark","controls.ListView_SetSelectionMark","controls._win32_ListView_SetSelectionMark"]
old-location: controls\ListView_SetSelectionMark.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setselectionmark.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetSelectionMark, ListView_SetSelectionMark macro [Windows Controls], _win32_ListView_SetSelectionMark, _win32_ListView_SetSelectionMark_cpp, commctrl/ListView_SetSelectionMark, controls.ListView_SetSelectionMark, controls._win32_ListView_SetSelectionMark
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
 - ListView_SetSelectionMark
 - commctrl/ListView_SetSelectionMark
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
 - ListView_SetSelectionMark
---

# ListView_SetSelectionMark macro

## -syntax

```cpp
INT ListView_SetSelectionMark(
   HWND hwnd,
   INT  i
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns the previous selection mark, or -1 if there is no previous selection mark.


## -description

Sets the selection mark in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setselectionmark">LVM_SETSELECTIONMARK</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

### -param i

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

the zero-based index of the list-view item to be selected.

## -remarks

The selection mark is the item index from which a multiple selection starts. This macro does not affect the selection state of the item.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_getselectionmark">ListView_GetSelectionMark</a>
