---
UID: NF:commctrl.ListView_GetTopIndex
title: ListView_GetTopIndex macro (commctrl.h)
description: Gets the index of the topmost visible item when in list or report view. You can use this macro or send the LVM_GETTOPINDEX message explicitly.
helpviewer_keywords: ["ListView_GetTopIndex","ListView_GetTopIndex macro [Windows Controls]","_win32_ListView_GetTopIndex","_win32_ListView_GetTopIndex_cpp","commctrl/ListView_GetTopIndex","controls.ListView_GetTopIndex","controls._win32_ListView_GetTopIndex"]
old-location: controls\ListView_GetTopIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettopindex.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetTopIndex, ListView_GetTopIndex macro [Windows Controls], _win32_ListView_GetTopIndex, _win32_ListView_GetTopIndex_cpp, commctrl/ListView_GetTopIndex, controls.ListView_GetTopIndex, controls._win32_ListView_GetTopIndex
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
 - ListView_GetTopIndex
 - commctrl/ListView_GetTopIndex
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
 - ListView_GetTopIndex
---

# ListView_GetTopIndex macro

## -syntax

```cpp
int ListView_GetTopIndex(
   HWND hwndLV
);
```

## -returns

Type: **int**

Returns the index of the item if successful, or zero if the list-view control is in icon or small icon view.


## -description

Gets the index of the topmost visible item when in list or report view. You can use this macro or send the <a href="/windows/desktop/controls/lvm-gettopindex">LVM_GETTOPINDEX</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
