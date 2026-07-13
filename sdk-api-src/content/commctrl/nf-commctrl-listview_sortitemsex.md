---
UID: NF:commctrl.ListView_SortItemsEx
title: ListView_SortItemsEx macro (commctrl.h)
description: Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the LVM_SORTITEMSEX message explicitly.
helpviewer_keywords: ["ListView_SortItemsEx","ListView_SortItemsEx macro [Windows Controls]","_win32_ListView_SortItemsEx","_win32_ListView_SortItemsEx_cpp","commctrl/ListView_SortItemsEx","controls.ListView_SortItemsEx","controls._win32_ListView_SortItemsEx"]
old-location: controls\ListView_SortItemsEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sortitemsex.htm
ms.date: 10/21/2024
ms.keywords: ListView_SortItemsEx, ListView_SortItemsEx macro [Windows Controls], _win32_ListView_SortItemsEx, _win32_ListView_SortItemsEx_cpp, commctrl/ListView_SortItemsEx, controls.ListView_SortItemsEx, controls._win32_ListView_SortItemsEx
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
 - ListView_SortItemsEx
 - commctrl/ListView_SortItemsEx
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
 - ListView_SortItemsEx
---

# ListView_SortItemsEx macro

## -syntax

```cpp
BOOL ListView_SortItemsEx(
   HWND         hwndLV,
   PFNLVCOMPARE _pfnCompare,
   LPARAM       _lPrm
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-sortitemsex">LVM_SORTITEMSEX</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param _pfnCompare

Type: <b>PFNLVCOMPARE</b>

A pointer to an application-defined comparison function. It is called during the sort operation each time the relative order of two list items needs to be compared.

### -param _lPrm

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The application-defined value that is passed to the comparison function.

## -remarks

The comparison function has the following form. 


``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM _lPrm);
```

where <i>lParam1</i> is the index of the first item and <i>lParam2</i> the index of the second. The <b>ListView_SortItemsEx</b>'s <i>_lPrm</i> parameter is passed to the callback function as its third parameter.

The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.

You can send an <a href="/windows/desktop/Controls/lvm-getitemtext">LVM_GETITEMTEXT</a> message to retrieve further information on an item, if needed.

This macro is similar to <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_sortitems">ListView_SortItems</a>, except for the type of information passed to the comparison function. With <b>ListView_SortItemsEx</b>, the item's index is passed instead of its <i>lparam</i> value.

<div class="alert"><b>Note</b>   During the sorting process, the list-view contents are unstable. If the callback function sends any messages to the list-view control aside from <a href="/windows/desktop/Controls/lvm-getitem">LVM_GETITEM</a> (<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_getitem">ListView_GetItem</a>), the results are unpredictable.</div>
<div> </div>
