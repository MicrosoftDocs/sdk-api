---
UID: NF:commctrl.TreeView_DeleteAllItems
title: TreeView_DeleteAllItems macro
author: windows-sdk-content
description: Deletes all items from a tree-view control.
old-location: controls\TreeView_DeleteAllItems.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_deleteallitems.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: TreeView_DeleteAllItems, TreeView_DeleteAllItems macro [Windows Controls], _win32_TreeView_DeleteAllItems, _win32_TreeView_DeleteAllItems_cpp, commctrl/TreeView_DeleteAllItems, controls.TreeView_DeleteAllItems, controls._win32_TreeView_DeleteAllItems
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
 - TreeView_DeleteAllItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_DeleteAllItems macro


## -description


Deletes all items from a tree-view control. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



Once an item is deleted from a tree-view control, its <b>HTREEITEM</b> handle is invalid and cannot be used.

The parent window receives a <a href="https://msdn.microsoft.com/library/Bb773512(v=VS.85).aspx">TVN_DELETEITEM</a> notification code when each item is removed.

If the item label is being edited, the edit operation is canceled and the parent window receives the <a href="https://msdn.microsoft.com/library/Bb773515(v=VS.85).aspx">TVN_ENDLABELEDIT</a> notification code. 

You can also delete all items with the <a href="https://msdn.microsoft.com/library/Bb773793(v=VS.85).aspx">TreeView_DeleteItem</a> macro or the <a href="https://msdn.microsoft.com/library/Bb773560(v=VS.85).aspx">TVM_DELETEITEM</a> message by setting 
				<i>lParam</i> to TVI_ROOT.

If the window style for a tree-view control contains TVS_NOSCROLL and all items are deleted, new items are not displayed until the window styles are reset. The following code shows one way to ensure that items are always displayed.


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DWORD styles = GetWindowLong(hwnd, GWL_STYLE);
TreeView_DeleteAllItems(hwnd);
SetWindowLong(hwnd, GWL_STYLE, styles);</pre>
</td>
</tr>
</table></span></div>


