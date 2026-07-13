---
UID: NF:commctrl.ListView_GetCountPerPage
title: ListView_GetCountPerPage macro (commctrl.h)
description: Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view. Only fully visible items are counted. You can use this macro or send the LVM_GETCOUNTPERPAGE message explicitly.
helpviewer_keywords: ["ListView_GetCountPerPage","ListView_GetCountPerPage macro [Windows Controls]","_win32_ListView_GetCountPerPage","_win32_ListView_GetCountPerPage_cpp","commctrl/ListView_GetCountPerPage","controls.ListView_GetCountPerPage","controls._win32_ListView_GetCountPerPage"]
old-location: controls\ListView_GetCountPerPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcountperpage.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetCountPerPage, ListView_GetCountPerPage macro [Windows Controls], _win32_ListView_GetCountPerPage, _win32_ListView_GetCountPerPage_cpp, commctrl/ListView_GetCountPerPage, controls.ListView_GetCountPerPage, controls._win32_ListView_GetCountPerPage
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
 - ListView_GetCountPerPage
 - commctrl/ListView_GetCountPerPage
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
 - ListView_GetCountPerPage
---

# ListView_GetCountPerPage macro

## -syntax

```cpp
int ListView_GetCountPerPage(
   HWND hwndLV
);
```

## -returns

Type: **int**

Returns the number of fully visible items if successful. If the current view is icon or small icon view, the return value is the total number of items in the list-view control.


## -description

Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view. Only fully visible items are counted. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getcountperpage">LVM_GETCOUNTPERPAGE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
