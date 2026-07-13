---
UID: NF:commctrl.ListView_InsertMarkHitTest
title: ListView_InsertMarkHitTest macro (commctrl.h)
description: Retrieves the insertion point closest to a specified point. You can use this macro or send the LVM_INSERTMARKHITTEST message explicitly.
helpviewer_keywords: ["ListView_InsertMarkHitTest","ListView_InsertMarkHitTest macro [Windows Controls]","_win32_ListView_InsertMarkHitTest","_win32_ListView_InsertMarkHitTest_cpp","commctrl/ListView_InsertMarkHitTest","controls.ListView_InsertMarkHitTest","controls._win32_ListView_InsertMarkHitTest"]
old-location: controls\ListView_InsertMarkHitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertmarkhittest.htm
ms.date: 10/21/2024
ms.keywords: ListView_InsertMarkHitTest, ListView_InsertMarkHitTest macro [Windows Controls], _win32_ListView_InsertMarkHitTest, _win32_ListView_InsertMarkHitTest_cpp, commctrl/ListView_InsertMarkHitTest, controls.ListView_InsertMarkHitTest, controls._win32_ListView_InsertMarkHitTest
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
 - ListView_InsertMarkHitTest
 - commctrl/ListView_InsertMarkHitTest
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
 - ListView_InsertMarkHitTest
---

# ListView_InsertMarkHitTest macro

## -syntax

```cpp
BOOL ListView_InsertMarkHitTest(
   HWND          hwnd,
   LPPOINT       point,
   PLVINSERTMARK lvim
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. 


## -description

Retrieves the insertion point closest to a specified point. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-insertmarkhittest">LVM_INSERTMARKHITTEST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param point

Type: <b>LPPOINT</b>

<b>POINT</b>

### -param lvim

Type: <b>PLVINSERTMARK</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>
<i>point</i>

## -remarks

To use <b>ListView_InsertMarkHitTest</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
