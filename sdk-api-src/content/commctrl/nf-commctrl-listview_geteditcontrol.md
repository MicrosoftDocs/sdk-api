---
UID: NF:commctrl.ListView_GetEditControl
title: ListView_GetEditControl macro (commctrl.h)
description: Gets the handle to the edit control being used to edit a list-view item's text. You can use this macro or send the LVM_GETEDITCONTROL message explicitly.
helpviewer_keywords: ["ListView_GetEditControl","ListView_GetEditControl macro [Windows Controls]","_win32_ListView_GetEditControl","_win32_ListView_GetEditControl_cpp","commctrl/ListView_GetEditControl","controls.ListView_GetEditControl","controls._win32_ListView_GetEditControl"]
old-location: controls\ListView_GetEditControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_geteditcontrol.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetEditControl, ListView_GetEditControl macro [Windows Controls], _win32_ListView_GetEditControl, _win32_ListView_GetEditControl_cpp, commctrl/ListView_GetEditControl, controls.ListView_GetEditControl, controls._win32_ListView_GetEditControl
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
 - ListView_GetEditControl
 - commctrl/ListView_GetEditControl
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
 - ListView_GetEditControl
---

# ListView_GetEditControl macro

## -syntax

```cpp
HWND ListView_GetEditControl(
   HWND hwndLV
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the edit control if successful, or <b>NULL</b> otherwise.


## -description

Gets the handle to the edit control being used to edit a list-view item's text. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-geteditcontrol">LVM_GETEDITCONTROL</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

When label editing begins, an edit control is created, positioned, and initialized. Before it is displayed, the list-view control sends its parent window an <a href="/windows/desktop/Controls/lvn-beginlabeledit">LVN_BEGINLABELEDIT</a> notification code. 

To customize label editing, implement a handler for <a href="/windows/desktop/Controls/lvn-beginlabeledit">LVN_BEGINLABELEDIT</a> and have it use <b>ListView_GetEditControl</b> to send an <a href="/windows/desktop/Controls/lvm-geteditcontrol">LVM_GETEDITCONTROL</a> message to the list-view control. If a label is being edited, the return value will be a handle to the edit control. Use this handle to customize the edit control by sending the usual 
				<b>EM_XXX</b> messages. 

When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but you should not destroy it. To cancel editing, you can send the list-view control a <a href="/windows/desktop/winmsg/wm-cancelmode">WM_CANCELMODE</a> message.

The list-view item being edited is the currently focused item—that is, the item in the focused state. To find an item based on its state, use the <a href="/windows/desktop/Controls/lvm-getnextitem">LVM_GETNEXTITEM</a> message.

## -see-also

<a href="/windows/desktop/Controls/lvm-geteditcontrol">LVM_GETEDITCONTROL</a>
