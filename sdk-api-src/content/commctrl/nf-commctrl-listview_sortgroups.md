---
UID: NF:commctrl.ListView_SortGroups
title: ListView_SortGroups macro (commctrl.h)
description: Uses an application-defined comparison function to sort groups by ID within a list-view control. You can use this macro or send the LVM_SORTGROUPS message explicitly.
helpviewer_keywords: ["ListView_SortGroups","ListView_SortGroups macro [Windows Controls]","_win32_ListView_SortGroups","_win32_ListView_SortGroups_cpp","commctrl/ListView_SortGroups","controls.ListView_SortGroups","controls._win32_ListView_SortGroups"]
old-location: controls\ListView_SortGroups.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sortgroups.htm
ms.date: 10/21/2024
ms.keywords: ListView_SortGroups, ListView_SortGroups macro [Windows Controls], _win32_ListView_SortGroups, _win32_ListView_SortGroups_cpp, commctrl/ListView_SortGroups, controls.ListView_SortGroups, controls._win32_ListView_SortGroups
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
 - ListView_SortGroups
 - commctrl/ListView_SortGroups
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
 - ListView_SortGroups
---

# ListView_SortGroups macro

## -syntax

```cpp
int ListView_SortGroups(
   HWND              hwnd,
   PFNLVGROUPCOMPARE _pfnGroupCompate,
   LPVOID            _plv
);
```

## -returns

Type: **int**

Returns 1 if successful, or 0 otherwise.


## -description

Uses an application-defined comparison function to sort groups by ID within a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-sortgroups">LVM_SORTGROUPS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param _pfnGroupCompate

Type: <b>PFNLVGROUPCOMPARE</b>

### -param _plv

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPVOID</a></b>

## -remarks

To use <b>ListView_SortGroups</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
