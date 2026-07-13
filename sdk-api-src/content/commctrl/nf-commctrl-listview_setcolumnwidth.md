---
UID: NF:commctrl.ListView_SetColumnWidth
title: ListView_SetColumnWidth macro (commctrl.h)
description: Used to change the width of a column in report view or the width of all columns in list-view mode. You can use this macro or send the LVM_SETCOLUMNWIDTH message explicitly.
helpviewer_keywords: ["LVSCW_AUTOSIZE","LVSCW_AUTOSIZE_USEHEADER","ListView_SetColumnWidth","ListView_SetColumnWidth macro [Windows Controls]","_win32_ListView_SetColumnWidth","_win32_ListView_SetColumnWidth_cpp","commctrl/ListView_SetColumnWidth","controls.ListView_SetColumnWidth","controls._win32_ListView_SetColumnWidth"]
old-location: controls\ListView_SetColumnWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcolumnwidth.htm
ms.date: 10/21/2024
ms.keywords: LVSCW_AUTOSIZE, LVSCW_AUTOSIZE_USEHEADER, ListView_SetColumnWidth, ListView_SetColumnWidth macro [Windows Controls], _win32_ListView_SetColumnWidth, _win32_ListView_SetColumnWidth_cpp, commctrl/ListView_SetColumnWidth, controls.ListView_SetColumnWidth, controls._win32_ListView_SetColumnWidth
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
 - ListView_SetColumnWidth
 - commctrl/ListView_SetColumnWidth
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
 - ListView_SetColumnWidth
---

# ListView_SetColumnWidth macro

## -syntax

```cpp
BOOL ListView_SetColumnWidth(
   HWND hwnd,
   int  iCol,
   int  cx
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Used to change the width of a column in report view or the width of all columns in list-view mode. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setcolumnwidth">LVM_SETCOLUMNWIDTH</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iCol

Type: <b>int</b>

The zero-based index of a valid column. For list-view mode, this parameter must be set to zero.

### -param cx

Type: <b>int</b>

The new width of the column, in pixels. For report-view mode, the following special values are supported: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVSCW_AUTOSIZE"></a><a id="lvscw_autosize"></a><dl>
<dt><b>LVSCW_AUTOSIZE</b></dt>
</dl>
</td>
<td width="60%">
Automatically sizes the column.

</td>
</tr>
<tr>
<td width="40%"><a id="LVSCW_AUTOSIZE_USEHEADER"></a><a id="lvscw_autosize_useheader"></a><dl>
<dt><b>LVSCW_AUTOSIZE_USEHEADER</b></dt>
</dl>
</td>
<td width="60%">
Automatically sizes the column to fit the header text. If you use this value with the last column, its width is set to fill the remaining width of the list-view control.

</td>
</tr>
</table>

## -remarks

Assume that you have a 2-column list-view control with a width of 500 pixels. If the width of column zero is set to 200 pixels, and you make the following call.

<code>ListView_SetColumnWidth(hwnd, 1, LVSCW_AUTOSIZE_USEHEADER)</code>

The second (and last) column will be 300 pixels wide.

Note that <b>ListView_SetColumnWidth</b> converts the 
				<i>cx</i> parameter to a 16-bit value.
