---
UID: NF:commctrl.ListView_GetInsertMarkRect
title: ListView_GetInsertMarkRect macro (commctrl.h)
description: Gets the rectangle that bounds the insertion point. You can use this macro or send the LVM_GETINSERTMARKRECT message explicitly.
helpviewer_keywords: ["ListView_GetInsertMarkRect","ListView_GetInsertMarkRect macro [Windows Controls]","_win32_ListView_GetInsertMarkRect","_win32_ListView_GetInsertMarkRect_cpp","commctrl/ListView_GetInsertMarkRect","controls.ListView_GetInsertMarkRect","controls._win32_ListView_GetInsertMarkRect"]
old-location: controls\ListView_GetInsertMarkRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmarkrect.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetInsertMarkRect, ListView_GetInsertMarkRect macro [Windows Controls], _win32_ListView_GetInsertMarkRect, _win32_ListView_GetInsertMarkRect_cpp, commctrl/ListView_GetInsertMarkRect, controls.ListView_GetInsertMarkRect, controls._win32_ListView_GetInsertMarkRect
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
 - ListView_GetInsertMarkRect
 - commctrl/ListView_GetInsertMarkRect
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
 - ListView_GetInsertMarkRect
---

# ListView_GetInsertMarkRect macro

## -syntax

```cpp
int ListView_GetInsertMarkRect(
   HWND   hwnd,
   LPRECT rc
);
```

## -returns

Type: **int**

Returns one of the following values:

| Return code | Description |
|---|---|
| 0 | No insertion point found. |
| 1 | Insertion point found. |

## -description

Gets the rectangle that bounds the insertion point. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getinsertmarkrect">LVM_GETINSERTMARKRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param rc

Type: <b>LPRECT</b>

<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>

## -remarks

To use <b>ListView_GetInsertMarkRect</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
