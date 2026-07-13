---
UID: NF:commctrl.ListView_GetInsertMarkColor
title: ListView_GetInsertMarkColor macro (commctrl.h)
description: Gets the color of the insertion point. You can use this macro or send the LVM_GETINSERTMARKCOLOR message explicitly.
helpviewer_keywords: ["ListView_GetInsertMarkColor","ListView_GetInsertMarkColor macro [Windows Controls]","_win32_ListView_GetInsertMarkColor","_win32_ListView_GetInsertMarkColor_cpp","commctrl/ListView_GetInsertMarkColor","controls.ListView_GetInsertMarkColor","controls._win32_ListView_GetInsertMarkColor"]
old-location: controls\ListView_GetInsertMarkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmarkcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetInsertMarkColor, ListView_GetInsertMarkColor macro [Windows Controls], _win32_ListView_GetInsertMarkColor, _win32_ListView_GetInsertMarkColor_cpp, commctrl/ListView_GetInsertMarkColor, controls.ListView_GetInsertMarkColor, controls._win32_ListView_GetInsertMarkColor
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
 - ListView_GetInsertMarkColor
 - commctrl/ListView_GetInsertMarkColor
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
 - ListView_GetInsertMarkColor
---

# ListView_GetInsertMarkColor macro

## -syntax

```cpp
COLORREF ListView_GetInsertMarkColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> structure that contains the color of the insertion point.


## -description

Gets the color of the insertion point. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getinsertmarkcolor">LVM_GETINSERTMARKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_GetInsertMarkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
