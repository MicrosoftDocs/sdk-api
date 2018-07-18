---
UID: NF:commctrl.TreeView_Select
title: TreeView_Select macro
author: windows-sdk-content
description: Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.
old-location: controls\TreeView_Select.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_select.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: TVGN_CARET, TVGN_DROPHILITE, TVGN_FIRSTVISIBLE, TreeView_Select, TreeView_Select macro [Windows Controls], _win32_TreeView_Select, _win32_TreeView_Select_cpp, commctrl/TreeView_Select, controls.TreeView_Select, controls._win32_TreeView_Select
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_Select
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_Select macro


## -description


Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation. You can use this macro or the <a href="https://msdn.microsoft.com/86f2b653-fde0-4c6c-9021-63f366723147">TreeView_SelectItem</a>, <a href="https://msdn.microsoft.com/12b304e5-0708-4d0e-a391-e6dd07609cda">TreeView_SelectSetFirstVisible</a>, or <a href="https://msdn.microsoft.com/ec35eade-b09f-4a5c-9525-326bdc9f6371">TreeView_SelectDropTarget</a> macros, or you can send the <a href="https://msdn.microsoft.com/8b943958-7b93-4e54-99de-200121cf0752">TVM_SELECTITEM</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item. 


### -param code

TBD






#### - flag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

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
Sets the selection to the given item. The control's parent window receives the <a href="https://msdn.microsoft.com/53f24ee0-433c-4680-9075-5e2b21117ed9">TVN_SELCHANGING</a> and <a href="https://msdn.microsoft.com/682170d3-5843-4d92-afeb-c37f3502ed5d">TVN_SELCHANGED</a> notification codes.

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
 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/18d9d61d-6ec5-4d3b-9c02-36d0e61ed232">TVN_ITEMEXPANDED</a> notification codes. 



