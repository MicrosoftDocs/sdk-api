---
UID: NF:commctrl.TreeView_Expand
title: TreeView_Expand macro
author: windows-sdk-content
description: The TreeView_Expand macro expands or collapses the list of child items associated with the specified parent item, if any. You can use this macro or send the TVM_EXPAND message explicitly.
old-location: controls\TreeView_Expand.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_expand.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: TreeView_Expand, TreeView_Expand macro [Windows Controls], _win32_TreeView_Expand, _win32_TreeView_Expand_cpp, commctrl/TreeView_Expand, controls.TreeView_Expand, controls._win32_TreeView_Expand
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
 - TreeView_Expand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_Expand macro


## -description


The <b>TreeView_Expand</b> macro expands or collapses the list of child items associated with the specified parent item, if any. You can use this macro or send the <a href="https://msdn.microsoft.com/d6c2e5b2-ce36-4c2b-b527-91c6de56e305">TVM_EXPAND</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the parent item that will be expanded or collapsed. 


### -param code

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Action flag. For a list of possible values, see the description of the <i>flag</i> parameter in <a href="https://msdn.microsoft.com/d6c2e5b2-ce36-4c2b-b527-91c6de56e305">TVM_EXPAND</a>. 


## -remarks



Expanding a node that is already expanded, or collapsing a node that is already collapsed is considered a successful operation and the macro returns a nonzero value. Attempting to expand or collapse a node that has no children is considered a failure and the return value is zero. 

When an item is first expanded by a <a href="https://msdn.microsoft.com/d6c2e5b2-ce36-4c2b-b527-91c6de56e305">TVM_EXPAND</a> message, the action generates <a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/18d9d61d-6ec5-4d3b-9c02-36d0e61ed232">TVN_ITEMEXPANDED</a> notification codes and the item's <a href="Tree_View_Control_Item_States.htm">TVIS_EXPANDEDONCE</a> state flag is set. As long as this state flag remains set, subsequent <b>TVM_EXPAND</b> messages do not generate TVN_ITEMEXPANDING or TVN_ITEMEXPANDED notifications. To reset the <b>TVIS_EXPANDEDONCE</b> state flag, you must send a <b>TVM_EXPAND</b> message with the TVE_COLLAPSE and TVE_COLLAPSERESET flags set. Attempting to explicitly set <b>TVIS_EXPANDEDONCE</b> will result in unpredictable behavior.

The expand operation may fail if the owner of the treeview control denies the operation in response to a <a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a> notification.



