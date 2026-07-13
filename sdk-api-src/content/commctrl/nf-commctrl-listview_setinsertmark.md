---
UID: NF:commctrl.ListView_SetInsertMark
title: ListView_SetInsertMark macro (commctrl.h)
description: Sets the insertion point to the defined position. You can use this macro or send the LVM_SETINSERTMARK message explicitly.
helpviewer_keywords: ["ListView_SetInsertMark","ListView_SetInsertMark macro [Windows Controls]","_win32_ListView_SetInsertMark","_win32_ListView_SetInsertMark_cpp","commctrl/ListView_SetInsertMark","controls.ListView_SetInsertMark","controls._win32_ListView_SetInsertMark"]
old-location: controls\ListView_SetInsertMark.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinsertmark.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetInsertMark, ListView_SetInsertMark macro [Windows Controls], _win32_ListView_SetInsertMark, _win32_ListView_SetInsertMark_cpp, commctrl/ListView_SetInsertMark, controls.ListView_SetInsertMark, controls._win32_ListView_SetInsertMark
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
 - ListView_SetInsertMark
 - commctrl/ListView_SetInsertMark
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
 - ListView_SetInsertMark
---

# ListView_SetInsertMark macro

## -syntax

```cpp
BOOL ListView_SetInsertMark(
   HWND          hwnd,
   PLVINSERTMARK lvim
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. Returns <b>FALSE</b> if the size of the <b>LVINSERTMARK</b> structure's <b>cbSize</b> member does not equal the actual size of the structure, or when an insertion point does not apply in the current view. 


## -description

Sets the insertion point to the defined position. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setinsertmark">LVM_SETINSERTMARK</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param lvim

Type: <b>PLVINSERTMARK</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>

## -remarks

To use <b>ListView_SetInsertMark</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
