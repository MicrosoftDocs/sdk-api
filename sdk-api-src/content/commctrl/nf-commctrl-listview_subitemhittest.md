---
UID: NF:commctrl.ListView_SubItemHitTest
title: ListView_SubItemHitTest macro (commctrl.h)
description: Determines which list-view item or subitem is located at a given position. You can use this macro or send the LVM_SUBITEMHITTEST message explicitly. (ListView_SubItemHitTest)
helpviewer_keywords: ["ListView_SubItemHitTest","ListView_SubItemHitTest macro [Windows Controls]","_win32_ListView_SubItemHitTest","_win32_ListView_SubItemHitTest_cpp","commctrl/ListView_SubItemHitTest","controls.ListView_SubItemHitTest","controls._win32_ListView_SubItemHitTest"]
old-location: controls\ListView_SubItemHitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_subitemhittest.htm
ms.date: 10/21/2024
ms.keywords: ListView_SubItemHitTest, ListView_SubItemHitTest macro [Windows Controls], _win32_ListView_SubItemHitTest, _win32_ListView_SubItemHitTest_cpp, commctrl/ListView_SubItemHitTest, controls.ListView_SubItemHitTest, controls._win32_ListView_SubItemHitTest
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
 - ListView_SubItemHitTest
 - commctrl/ListView_SubItemHitTest
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
 - ListView_SubItemHitTest
---

# ListView_SubItemHitTest macro

## -syntax

```cpp
INT ListView_SubItemHitTest(
   HWND            hwnd,
   LPLVHITTESTINFO plvhti
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns the index of the item or subitem tested, if any, or -1 otherwise. If an item or subitem is at the given coordinates, the fields of the <b>LVHITTESTINFO</b> structure will be filled with the applicable hit information.


## -description

Determines which list-view item or subitem is located at a given position. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-subitemhittest">LVM_SUBITEMHITTEST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control that will be hit-tested.

### -param plvhti

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvhittestinfo">LVHITTESTINFO</a> structure. The <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure within <b>LVHITTESTINFO</b> must be set to the client coordinates to be hit-tested.
