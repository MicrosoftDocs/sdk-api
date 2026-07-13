---
UID: NF:commctrl.ListView_HasGroup
title: ListView_HasGroup macro (commctrl.h)
description: Determines whether the list-view control has a specified group. You can use this macro or send the LVM_HASGROUP message explicitly.
helpviewer_keywords: ["ListView_HasGroup","ListView_HasGroup macro [Windows Controls]","_win32_ListView_HasGroup","_win32_ListView_HasGroup_cpp","commctrl/ListView_HasGroup","controls.ListView_HasGroup","controls._win32_ListView_HasGroup"]
old-location: controls\ListView_HasGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_hasgroup.htm
ms.date: 10/21/2024
ms.keywords: ListView_HasGroup, ListView_HasGroup macro [Windows Controls], _win32_ListView_HasGroup, _win32_ListView_HasGroup_cpp, commctrl/ListView_HasGroup, controls.ListView_HasGroup, controls._win32_ListView_HasGroup
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
 - ListView_HasGroup
 - commctrl/ListView_HasGroup
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
 - ListView_HasGroup
---

# ListView_HasGroup macro

## -syntax

```cpp
BOOL ListView_HasGroup(
   HWND hwnd,
   int  dwGroupId
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if the list-view control has the specified group, or <b>FALSE</b> otherwise.


## -description

Determines whether the list-view control has a specified group. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-hasgroup">LVM_HASGROUP</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param dwGroupId

Type: <b>int</b>

## -remarks

To use <b>ListView_HasGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
