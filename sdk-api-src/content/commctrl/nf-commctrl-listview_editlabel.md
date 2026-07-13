---
UID: NF:commctrl.ListView_EditLabel
title: ListView_EditLabel macro (commctrl.h)
description: Begins in-place editing of the specified list-view item's text. The message implicitly selects and focuses the specified item. You can use this macro or send the LVM_EDITLABEL message explicitly.
helpviewer_keywords: ["ListView_EditLabel","ListView_EditLabel macro [Windows Controls]","_win32_ListView_EditLabel","_win32_ListView_EditLabel_cpp","commctrl/ListView_EditLabel","controls.ListView_EditLabel","controls._win32_ListView_EditLabel"]
old-location: controls\ListView_EditLabel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_editlabel.htm
ms.date: 10/21/2024
ms.keywords: ListView_EditLabel, ListView_EditLabel macro [Windows Controls], _win32_ListView_EditLabel, _win32_ListView_EditLabel_cpp, commctrl/ListView_EditLabel, controls.ListView_EditLabel, controls._win32_ListView_EditLabel
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
 - ListView_EditLabel
 - commctrl/ListView_EditLabel
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
 - ListView_EditLabel
---

# ListView_EditLabel macro

## -syntax

```cpp
HWND ListView_EditLabel(
   HWND hwndLV,
   int  i
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the edit control that is used to edit the item text if successful, or <b>NULL</b> otherwise.


## -description

Begins in-place editing of the specified list-view item's text. The message implicitly selects and focuses the specified item. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-editlabel">LVM_EDITLABEL</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the list-view item. To cancel editing, set <i>i</i> to -1.

## -remarks

When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but you should not destroy it. 

The control must have the focus before you send this message to the control. Focus can be set using the <a href="/windows/desktop/api/winuser/nf-winuser-setfocus">SetFocus</a> function.

## -see-also

<a href="/windows/desktop/winmsg/wm-cancelmode">WM_CANCELMODE</a>
