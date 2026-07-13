---
UID: NF:commctrl.ListView_GetExtendedListViewStyle
title: ListView_GetExtendedListViewStyle macro (commctrl.h)
description: Gets the extended styles that are currently in use for a given list-view control. You can use this macro or send the LVM_GETEXTENDEDLISTVIEWSTYLE message explicitly.
helpviewer_keywords: ["ListView_GetExtendedListViewStyle","ListView_GetExtendedListViewStyle macro [Windows Controls]","_win32_ListView_GetExtendedListViewStyle","_win32_ListView_GetExtendedListViewStyle_cpp","commctrl/ListView_GetExtendedListViewStyle","controls.ListView_GetExtendedListViewStyle","controls._win32_ListView_GetExtendedListViewStyle"]
old-location: controls\ListView_GetExtendedListViewStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getextendedlistviewstyle.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetExtendedListViewStyle, ListView_GetExtendedListViewStyle macro [Windows Controls], _win32_ListView_GetExtendedListViewStyle, _win32_ListView_GetExtendedListViewStyle_cpp, commctrl/ListView_GetExtendedListViewStyle, controls.ListView_GetExtendedListViewStyle, controls._win32_ListView_GetExtendedListViewStyle
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
 - ListView_GetExtendedListViewStyle
 - commctrl/ListView_GetExtendedListViewStyle
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
 - ListView_GetExtendedListViewStyle
---

# ListView_GetExtendedListViewStyle macro

## -syntax

```cpp
DWORD ListView_GetExtendedListViewStyle(
   HWND hwndLV
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that represents the styles currently in use for a given list-view control. This can be a combination of extended styles.


## -description

Gets the extended styles that are currently in use for a given list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getextendedlistviewstyle">LVM_GETEXTENDEDLISTVIEWSTYLE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.
