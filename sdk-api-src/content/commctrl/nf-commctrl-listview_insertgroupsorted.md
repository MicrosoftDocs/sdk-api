---
UID: NF:commctrl.ListView_InsertGroupSorted
title: ListView_InsertGroupSorted macro (commctrl.h)
description: Inserts a group into an ordered list of groups. You can use this macro or send the LVM_INSERTGROUPSORTED message explicitly.
helpviewer_keywords: ["ListView_InsertGroupSorted","ListView_InsertGroupSorted macro [Windows Controls]","_win32_ListView_InsertGroupSorted","_win32_ListView_InsertGroupSorted_cpp","commctrl/ListView_InsertGroupSorted","controls.ListView_InsertGroupSorted","controls._win32_ListView_InsertGroupSorted"]
old-location: controls\ListView_InsertGroupSorted.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertgroupsorted.htm
ms.date: 10/21/2024
ms.keywords: ListView_InsertGroupSorted, ListView_InsertGroupSorted macro [Windows Controls], _win32_ListView_InsertGroupSorted, _win32_ListView_InsertGroupSorted_cpp, commctrl/ListView_InsertGroupSorted, controls.ListView_InsertGroupSorted, controls._win32_ListView_InsertGroupSorted
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
 - ListView_InsertGroupSorted
 - commctrl/ListView_InsertGroupSorted
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
 - ListView_InsertGroupSorted
---

# ListView_InsertGroupSorted macro

## -syntax

```cpp
void ListView_InsertGroupSorted(
   HWND                 hwnd,
   PLVINSERTGROUPSORTED structInsert
);
```


## -description

Inserts a group into an ordered list of groups. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-insertgroupsorted">LVM_INSERTGROUPSORTED</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param structInsert

Type: <b>PLVINSERTGROUPSORTED</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a>

## -remarks

To use <b>ListView_InsertGroupSorted</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
