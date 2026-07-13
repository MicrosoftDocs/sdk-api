---
UID: NF:commctrl.ListView_SortItems
title: ListView_SortItems macro (commctrl.h)
description: Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the LVM_SORTITEMS message explicitly.
helpviewer_keywords: ["ListView_SortItems","ListView_SortItems macro [Windows Controls]","_win32_ListView_SortItems","_win32_ListView_SortItems_cpp","commctrl/ListView_SortItems","controls.ListView_SortItems","controls._win32_ListView_SortItems"]
old-location: controls\ListView_SortItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sortitems.htm
ms.date: 10/21/2024
ms.keywords: ListView_SortItems, ListView_SortItems macro [Windows Controls], _win32_ListView_SortItems, _win32_ListView_SortItems_cpp, commctrl/ListView_SortItems, controls.ListView_SortItems, controls._win32_ListView_SortItems
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
 - ListView_SortItems
 - commctrl/ListView_SortItems
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
 - ListView_SortItems
---

# ListView_SortItems macro

## -syntax

```cpp
BOOL ListView_SortItems(
   HWND         hwndLV,
   PFNLVCOMPARE _pfnCompare,
   LPARAM       _lPrm
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-sortitems">LVM_SORTITEMS</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param _pfnCompare

Type: <b>PFNLVCOMPARE</b>

A pointer to the application-defined comparison function. The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.

### -param _lPrm

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The application-defined value that is passed to the comparison function.

## -remarks

The comparison function has the following form.


``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM _lPrm);
```

The <i>lParam1</i> parameter is the value associated with the first item being compared; and the <i>lParam2</i> parameter is the value associated with the second item. These are the values that were specified in the <b>lParam</b> member of the items' <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure when they were inserted into the list. The <i>_lPrm</i> parameter is the same value passed to the <a href="/windows/desktop/Controls/lvm-sortitems">LVM_SORTITEMS</a> message.

The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.

<div class="alert"><b>Note</b>   During the sorting process, the list-view contents are unstable. If the callback function sends any messages to the list-view control, the results are unpredictable.</div>
<div> </div>
