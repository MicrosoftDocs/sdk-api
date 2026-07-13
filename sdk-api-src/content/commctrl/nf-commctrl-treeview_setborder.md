---
UID: NF:commctrl.TreeView_SetBorder
title: TreeView_SetBorder macro (commctrl.h)
description: Sets the size of the border for the items in a tree-view control. You can use this macro or send the TVM_SETBORDER message explicitly.
helpviewer_keywords: ["TVSBF_XBORDER","TVSBF_YBORDER","TreeView_SetBorder","TreeView_SetBorder macro [Windows Controls]","_win32_TreeView_SetBorder","_win32_TreeView_SetBorder_cpp","commctrl/TreeView_SetBorder","controls.TreeView_SetBorder","controls._win32_TreeView_SetBorder"]
old-location: controls\TreeView_SetBorder.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setborder.htm
ms.date: 10/21/2024
ms.keywords: TVSBF_XBORDER, TVSBF_YBORDER, TreeView_SetBorder, TreeView_SetBorder macro [Windows Controls], _win32_TreeView_SetBorder, _win32_TreeView_SetBorder_cpp, commctrl/TreeView_SetBorder, controls.TreeView_SetBorder, controls._win32_TreeView_SetBorder
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
 - TreeView_SetBorder
 - commctrl/TreeView_SetBorder
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
 - TreeView_SetBorder
---

# TreeView_SetBorder macro

## -syntax

```cpp
int TreeView_SetBorder(
   HWND  hwnd,
   DWORD dwFlags,
   SHORT xBorder,
   SHORT yBorder
);
```

## -returns

Type: **int**

Returns a <b>int</b> value that contains the previous border size, in pixels. The <b>LOWORD</b> contains the previous size of the horizontal border, and the <b>HIWORD</b> contains the previous size of the vertical border.


## -description

<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Sets the size of the border for the items in a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setborder">TVM_SETBORDER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Action flags. This parameter can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVSBF_XBORDER"></a><a id="tvsbf_xborder"></a><dl>
<dt><b>TVSBF_XBORDER</b></dt>
</dl>
</td>
<td width="60%">
Applies the specified border size to the left side of the items in the tree-view control.

</td>
</tr>
<tr>
<td width="40%"><a id="TVSBF_YBORDER"></a><a id="tvsbf_yborder"></a><dl>
<dt><b>TVSBF_YBORDER</b></dt>
</dl>
</td>
<td width="60%">
Applies the specified border size to the top of the items in the tree-view control.

</td>
</tr>
</table>

### -param xBorder

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Size of the left border, in pixels.

### -param yBorder

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Size of the top border, in pixels.

## -remarks

The item border is set just for spacing purposes. A successful setting triggers a recalculation of the scroll bars.

## -see-also

<a href="/windows/desktop/Controls/tvm-setborder">TVM_SETBORDER</a>
