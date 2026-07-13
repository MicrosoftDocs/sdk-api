---
UID: NF:commctrl.ListView_GetView
title: ListView_GetView macro (commctrl.h)
description: Gets the current view of a list-view control. You can use this macro or send the LVM_GETVIEW message explicitly.
helpviewer_keywords: ["ListView_GetView","ListView_GetView macro [Windows Controls]","_win32_ListView_GetView","_win32_ListView_GetView_cpp","commctrl/ListView_GetView","controls.ListView_GetView","controls._win32_ListView_GetView"]
old-location: controls\ListView_GetView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getview.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetView, ListView_GetView macro [Windows Controls], _win32_ListView_GetView, _win32_ListView_GetView_cpp, commctrl/ListView_GetView, controls.ListView_GetView, controls._win32_ListView_GetView
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
 - ListView_GetView
 - commctrl/ListView_GetView
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
 - ListView_GetView
---

# ListView_GetView macro

## -syntax

```cpp
DWORD ListView_GetView(
   HWND hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> that specifies the current view.


## -description

Gets the current view of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getview">LVM_GETVIEW</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_GetView</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
