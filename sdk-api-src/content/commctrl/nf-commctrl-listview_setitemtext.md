---
UID: NF:commctrl.ListView_SetItemText
title: ListView_SetItemText macro (commctrl.h)
description: Changes the text of a list-view item or subitem. You can use this macro or send the LVM_SETITEMTEXT message explicitly.
helpviewer_keywords: ["ListView_SetItemText","ListView_SetItemText macro [Windows Controls]","_win32_ListView_SetItemText","_win32_ListView_SetItemText_cpp","commctrl/ListView_SetItemText","controls.ListView_SetItemText","controls._win32_ListView_SetItemText"]
old-location: controls\ListView_SetItemText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemtext.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetItemText, ListView_SetItemText macro [Windows Controls], _win32_ListView_SetItemText, _win32_ListView_SetItemText_cpp, commctrl/ListView_SetItemText, controls.ListView_SetItemText, controls._win32_ListView_SetItemText
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
 - ListView_SetItemText
 - commctrl/ListView_SetItemText
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
 - ListView_SetItemText
---
# ListView_SetItemText macro

## -syntax

```cpp
VOID ListView_SetItemText(
   HWND    hwndLV,
   int     i,
   int     iSubItem_,
   LPCTSTR pszText_
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.

## -description

Changes the text of a list-view item or subitem. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setitemtext">LVM_SETITEMTEXT</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The zero-based index of the list-view item.

### -param iSubItem_

Type: <b>int</b>

The one-based index of the subitem. To set the item label, set <i>iSubItem_</i> to zero.

### -param pszText_

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the new text. This parameter can be LPSTR_TEXTCALLBACK to indicate a callback item for which the parent window stores the text. In this case, the list-view control sends the parent an <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> notification code when it needs the text.

This parameter can be <b>NULL</b>.
