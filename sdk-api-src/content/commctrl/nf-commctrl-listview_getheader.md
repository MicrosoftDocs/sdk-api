---
UID: NF:commctrl.ListView_GetHeader
title: ListView_GetHeader macro (commctrl.h)
description: Gets the handle to the header control used by a list-view control. You can use this macro or send the LVM_GETHEADER message explicitly.
helpviewer_keywords: ["ListView_GetHeader","ListView_GetHeader macro [Windows Controls]","_win32_ListView_GetHeader","_win32_ListView_GetHeader_cpp","commctrl/ListView_GetHeader","controls.ListView_GetHeader","controls._win32_ListView_GetHeader"]
old-location: controls\ListView_GetHeader.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getheader.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetHeader, ListView_GetHeader macro [Windows Controls], _win32_ListView_GetHeader, _win32_ListView_GetHeader_cpp, commctrl/ListView_GetHeader, controls.ListView_GetHeader, controls._win32_ListView_GetHeader
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
 - ListView_GetHeader
 - commctrl/ListView_GetHeader
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
 - ListView_GetHeader
---

# ListView_GetHeader macro

## -syntax

```cpp
HWND ListView_GetHeader(
   HWND hwnd
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the header control.


## -description

Gets the handle to the header control used by a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getheader">LVM_GETHEADER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.
