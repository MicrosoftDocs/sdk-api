---
UID: NF:commctrl.TreeView_GetNextItem
title: TreeView_GetNextItem macro
author: windows-sdk-content
description: Retrieves the tree-view item that bears the specified relationship to a specified item. You can use this macro, use one of the TreeView_Get macros described below, or send the TVM_GETNEXTITEM message explicitly.
old-location: controls\TreeView_GetNextItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getnextitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TVGN_CARET, TVGN_CHILD, TVGN_DROPHILITE, TVGN_FIRSTVISIBLE, TVGN_NEXT, TVGN_NEXTSELECTED, TVGN_NEXTVISIBLE, TVGN_PARENT, TVGN_PREVIOUS, TVGN_PREVIOUSVISIBLE, TVGN_ROOT, TreeView_GetNextItem, TreeView_GetNextItem macro [Windows Controls], _win32_TreeView_GetNextItem, _win32_TreeView_GetNextItem_cpp, commctrl/TreeView_GetNextItem, controls.TreeView_GetNextItem, controls._win32_TreeView_GetNextItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_GetNextItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- TreeView_GetNextItem
: 
---

# TreeView_GetNextItem macro


## -description


Retrieves the tree-view item that bears the specified relationship to a specified item. You can use this macro, use one of the 
			<b>TreeView_Get</b> macros described below, or send the <a href="https://msdn.microsoft.com/505c713c-7728-4119-bc0e-482fe7e73193">TVM_GETNEXTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. 


### -param code

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flag specifying the item to retrieve. This parameter can be one of the following values: 

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
Retrieves the currently selected item. You can use the <a href="https://msdn.microsoft.com/938598b4-37ed-4197-bb0d-73c29f990f5d">TreeView_GetSelection</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_CHILD"></a><a id="tvgn_child"></a><dl>
<dt><b>TVGN_CHILD</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the first child item of the item specified by the 
						<i>hitem</i> parameter. You can use the <a href="https://msdn.microsoft.com/49eb25c4-52b3-4b3a-ae2f-433af9adf0d4">TreeView_GetChild</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_DROPHILITE"></a><a id="tvgn_drophilite"></a><dl>
<dt><b>TVGN_DROPHILITE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the item that is the target of a drag-and-drop operation. You can use the <a href="https://msdn.microsoft.com/e8c9cc6d-c840-47d9-8890-539bc674ec77">TreeView_GetDropHilight</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_FIRSTVISIBLE"></a><a id="tvgn_firstvisible"></a><dl>
<dt><b>TVGN_FIRSTVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the first visible item. You can use the <a href="https://msdn.microsoft.com/9da74062-e029-4c73-821f-829a0964afba">TreeView_GetFirstVisible</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_NEXT"></a><a id="tvgn_next"></a><dl>
<dt><b>TVGN_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the next sibling item. You can use the <a href="https://msdn.microsoft.com/1fe480ea-dcb5-4d08-8eec-996f78757fda">TreeView_GetNextSibling</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_NEXTSELECTED"></a><a id="tvgn_nextselected"></a><dl>
<dt><b>TVGN_NEXTSELECTED</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later.</b> Retrieves the next selected item. You can use the <a href="https://msdn.microsoft.com/62db774a-5ac5-49d1-a05b-c7c53944270a">TreeView_GetNextSelected</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_NEXTVISIBLE"></a><a id="tvgn_nextvisible"></a><dl>
<dt><b>TVGN_NEXTVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the next visible item that follows the specified item. The specified item must be visible. Use the <a href="https://msdn.microsoft.com/f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c">TVM_GETITEMRECT</a> message to determine whether an item is visible. You can use the <a href="https://msdn.microsoft.com/7e21cd1b-d05e-4c62-9ec8-244a096f90f3">TreeView_GetNextVisible</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_PARENT"></a><a id="tvgn_parent"></a><dl>
<dt><b>TVGN_PARENT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the parent of the specified item. You can use the <a href="https://msdn.microsoft.com/a286e32f-d152-4cd9-b7fc-75d946378c34">TreeView_GetParent</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_PREVIOUS"></a><a id="tvgn_previous"></a><dl>
<dt><b>TVGN_PREVIOUS</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the previous sibling item. You can use the <a href="https://msdn.microsoft.com/2f013ffb-43dd-460f-824a-36fb67639834">TreeView_GetPrevSibling</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_PREVIOUSVISIBLE"></a><a id="tvgn_previousvisible"></a><dl>
<dt><b>TVGN_PREVIOUSVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the first visible item that precedes the specified item. The specified item must be visible. Use the <a href="https://msdn.microsoft.com/f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c">TVM_GETITEMRECT</a> message to determine whether an item is visible. You can use the <a href="https://msdn.microsoft.com/b9a4ad11-bd4a-48c6-9dbb-a92a3e410dc3">TreeView_GetPrevVisible</a> macro to send this message.

</td>
</tr>
<tr>
<td width="40%"><a id="TVGN_ROOT"></a><a id="tvgn_root"></a><dl>
<dt><b>TVGN_ROOT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the topmost or very first item of the tree-view control. You can use the <a href="https://msdn.microsoft.com/419dd3d8-06df-4d95-b589-00dfabc95f77">TreeView_GetRoot</a> macro to send this message. 

</td>
</tr>
</table>
 


## -remarks



This macro will return <b>NULL</b> if the item being retrieved is the root node of the tree. For example, if you use this macro with the TVGN_PARENT flag on a first-level child of the tree view's root node, the macro will return <b>NULL</b>.



