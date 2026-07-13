---
UID: NF:commctrl.ListView_SetView
title: ListView_SetView macro (commctrl.h)
description: Sets the view of a list-view control. You can use this macro or send the LVM_SETVIEW message explicitly.
helpviewer_keywords: ["ListView_SetView","ListView_SetView macro [Windows Controls]","_win32_ListView_SetView","_win32_ListView_SetView_cpp","commctrl/ListView_SetView","controls.ListView_SetView","controls._win32_ListView_SetView"]
old-location: controls\ListView_SetView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setview.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetView, ListView_SetView macro [Windows Controls], _win32_ListView_SetView, _win32_ListView_SetView_cpp, commctrl/ListView_SetView, controls.ListView_SetView, controls._win32_ListView_SetView
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
 - ListView_SetView
 - commctrl/ListView_SetView
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
 - ListView_SetView
---

# ListView_SetView macro

## -syntax

```cpp
DWORD ListView_SetView(
   HWND  hwnd,
   DWORD iView
);
```

## -returns

Type: **DWORD**

Returns 1 if successful, or UINT_MAX otherwise. For example, returns UINT_MAX if the view is invalid.


## -description

Sets the view of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setview">LVM_SETVIEW</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iView

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b>
<a href="/windows/desktop/Controls/lvm-setview">LVM_SETVIEW</a>

## -remarks

To use <b>ListView_SetView</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
