---
UID: NF:commctrl.ListView_InsertGroup
title: ListView_InsertGroup macro (commctrl.h)
description: Inserts a group into a list-view control. You can use this macro or send the LVM_INSERTGROUP message explicitly.
helpviewer_keywords: ["ListView_InsertGroup","ListView_InsertGroup macro [Windows Controls]","_win32_ListView_InsertGroup","_win32_ListView_InsertGroup_cpp","commctrl/ListView_InsertGroup","controls.ListView_InsertGroup","controls._win32_ListView_InsertGroup"]
old-location: controls\ListView_InsertGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertgroup.htm
ms.date: 10/21/2024
ms.keywords: ListView_InsertGroup, ListView_InsertGroup macro [Windows Controls], _win32_ListView_InsertGroup, _win32_ListView_InsertGroup_cpp, commctrl/ListView_InsertGroup, controls.ListView_InsertGroup, controls._win32_ListView_InsertGroup
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
 - ListView_InsertGroup
 - commctrl/ListView_InsertGroup
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
 - ListView_InsertGroup
---

# ListView_InsertGroup macro

## -syntax

```cpp
int ListView_InsertGroup(
   HWND     hwnd,
   int      index,
   PLVGROUP pgrp
);
```

## -returns

Type: **int**

Returns the index of the item that the group was added to, or -1 if the operation failed.


## -description

Inserts a group into a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-insertgroup">LVM_INSERTGROUP</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param index

Type: <b>int</b>

### -param pgrp

Type: <b>PLVGROUP</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a>

## -remarks

To turn on group mode, call <a href="/windows/desktop/Controls/lvm-enablegroupview">LVM_ENABLEGROUPVIEW</a> or <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_enablegroupview">ListView_EnableGroupView</a>.


To use <b>ListView_InsertGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
