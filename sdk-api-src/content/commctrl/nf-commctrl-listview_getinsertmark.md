---
UID: NF:commctrl.ListView_GetInsertMark
title: ListView_GetInsertMark macro (commctrl.h)
description: Gets the position of the insertion point. You can use this macro or send the LVM_GETINSERTMARK message explicitly.
helpviewer_keywords: ["ListView_GetInsertMark","ListView_GetInsertMark macro [Windows Controls]","_win32_ListView_GetInsertMark","_win32_ListView_GetInsertMark_cpp","commctrl/ListView_GetInsertMark","controls.ListView_GetInsertMark","controls._win32_ListView_GetInsertMark"]
old-location: controls\ListView_GetInsertMark.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmark.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetInsertMark, ListView_GetInsertMark macro [Windows Controls], _win32_ListView_GetInsertMark, _win32_ListView_GetInsertMark_cpp, commctrl/ListView_GetInsertMark, controls.ListView_GetInsertMark, controls._win32_ListView_GetInsertMark
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
 - ListView_GetInsertMark
 - commctrl/ListView_GetInsertMark
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
 - ListView_GetInsertMark
---

# ListView_GetInsertMark macro

## -syntax

```cpp
BOOL ListView_GetInsertMark(
   HWND          hwnd,
   PLVINSERTMARK lvim
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. Returns <b>FALSE</b> if the size in the <b>cbSize</b> member of the <b>LVINSERTMARK</b> structure does not equal the actual size of the structure.


## -description

Gets the position of the insertion point. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getinsertmark">LVM_GETINSERTMARK</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param lvim

Type: <b>PLVINSERTMARK</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>

## -remarks

To use <b>ListView_GetInsertMark</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
