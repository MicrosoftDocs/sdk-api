---
UID: NF:commctrl.ListView_SetExtendedListViewStyleEx
title: ListView_SetExtendedListViewStyleEx macro (commctrl.h)
description: Sets extended styles for list-view controls using the style mask. You can use this macro or send the LVM_SETEXTENDEDLISTVIEWSTYLE message explicitly.
helpviewer_keywords: ["ListView_SetExtendedListViewStyleEx","ListView_SetExtendedListViewStyleEx macro [Windows Controls]","_win32_ListView_SetExtendedListViewStyleEx","_win32_ListView_SetExtendedListViewStyleEx_cpp","commctrl/ListView_SetExtendedListViewStyleEx","controls.ListView_SetExtendedListViewStyleEx","controls._win32_ListView_SetExtendedListViewStyleEx"]
old-location: controls\ListView_SetExtendedListViewStyleEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setextendedlistviewstyleex.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetExtendedListViewStyleEx, ListView_SetExtendedListViewStyleEx macro [Windows Controls], _win32_ListView_SetExtendedListViewStyleEx, _win32_ListView_SetExtendedListViewStyleEx_cpp, commctrl/ListView_SetExtendedListViewStyleEx, controls.ListView_SetExtendedListViewStyleEx, controls._win32_ListView_SetExtendedListViewStyleEx
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
 - ListView_SetExtendedListViewStyleEx
 - commctrl/ListView_SetExtendedListViewStyleEx
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
 - ListView_SetExtendedListViewStyleEx
---

# ListView_SetExtendedListViewStyleEx macro

## -syntax

```cpp
void ListView_SetExtendedListViewStyleEx(
   HWND  hwndLV,
   DWORD dwMask,
   DWORD dw
);
```


## -description

Sets extended styles for list-view controls using the style mask. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setextendedlistviewstyle">LVM_SETEXTENDEDLISTVIEWSTYLE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control that will receive the style change.

### -param dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A <b>DWORD</b> value that specifies which styles in <i>dw</i> are to be affected. This parameter can be a combination of <a href="/windows/desktop/Controls/extended-list-view-styles">Extended List-View Styles</a>. Only the extended styles in <i>dwMask</i> will be changed. All other styles will be maintained as they are. If this parameter is zero, all of the styles in <i>dw</i> will be affected.

### -param dw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A <b>DWORD</b> value that specifies the extended list-view control styles to set. This parameter can be a combination of <a href="/windows/desktop/Controls/extended-list-view-styles">Extended List-View Styles</a>. Styles that are not set, but that are specified in <i>dwMask</i>, are removed.

## -remarks

When you use this macro to set the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_CHECKBOXES</a> style, any previously set state image index will be discarded. All check boxes will be initialized to the unchecked state. The state image index is contained in bits 12 through 15 of the <b>state</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure.
