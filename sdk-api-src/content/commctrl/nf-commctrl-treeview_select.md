---
UID: NF:commctrl.TreeView_Select
title: TreeView_Select macro (commctrl.h)
description: Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.
helpviewer_keywords: ["TVGN_CARET","TVGN_DROPHILITE","TVGN_FIRSTVISIBLE","TreeView_Select","TreeView_Select macro [Windows Controls]","_win32_TreeView_Select","_win32_TreeView_Select_cpp","commctrl/TreeView_Select","controls.TreeView_Select","controls._win32_TreeView_Select"]
old-location: controls\TreeView_Select.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_select.htm
ms.date: 10/21/2024
ms.keywords: TVGN_CARET, TVGN_DROPHILITE, TVGN_FIRSTVISIBLE, TreeView_Select, TreeView_Select macro [Windows Controls], _win32_TreeView_Select, _win32_TreeView_Select_cpp, commctrl/TreeView_Select, controls.TreeView_Select, controls._win32_TreeView_Select
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
 - TreeView_Select
 - commctrl/TreeView_Select
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
 - TreeView_Select
---

# TreeView_Select macro

## -syntax

```cpp
BOOL TreeView_Select(
   HWND      hwnd,
   HTREEITEM hitem,
   UINT      code
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation. You can use this macro or the <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_selectitem">TreeView_SelectItem</a>, <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_selectsetfirstvisible">TreeView_SelectSetFirstVisible</a>, or <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_selectdroptarget">TreeView_SelectDropTarget</a> macros, or you can send the <a href="/windows/desktop/Controls/tvm-selectitem">TVM_SELECTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item.

### -param code

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Action flag. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVGN_CARET"></a><a id="tvgn_caret"></a><dl>
<dt><b>TVGN_CARET</b></dt>
</dl>
</td>
<td width="60%">
Sets the selection to the given item. The control's parent window receives the <a href="/windows/desktop/Controls/tvn-selchanging">TVN_SELCHANGING</a> and <a href="/windows/desktop/Controls/tvn-selchanged">TVN_SELCHANGED</a> notification codes.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_DROPHILITE"></a><a id="tvgn_drophilite"></a><dl>
<dt><b>TVGN_DROPHILITE</b></dt>
</dl>
</td>
<td width="60%">
Redraws the given item in the style used to indicate the target of a drag-and-drop operation.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_FIRSTVISIBLE"></a><a id="tvgn_firstvisible"></a><dl>
<dt><b>TVGN_FIRSTVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window. Tree-view controls display as many items as will fit in the window. If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.

</td>
</tr>
</table>

## -remarks

If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a> and <a href="/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a> notification codes.
