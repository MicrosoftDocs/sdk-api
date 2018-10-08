---
UID: NF:commctrl.TreeView_SelectDropTarget
title: TreeView_SelectDropTarget macro
author: windows-sdk-content
description: Redraws a specified tree-view control item in the style used to indicate the target of a drag-and-drop operation. You can use this macro or the TreeView_Select macro, or you can send the TVM_SELECTITEM message explicitly.
old-location: controls\TreeView_SelectDropTarget.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_selectdroptarget.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: TreeView_SelectDropTarget, TreeView_SelectDropTarget macro [Windows Controls], _win32_TreeView_SelectDropTarget, _win32_TreeView_SelectDropTarget_cpp, commctrl/TreeView_SelectDropTarget, controls.TreeView_SelectDropTarget, controls._win32_TreeView_SelectDropTarget
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
 - TreeView_SelectDropTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SelectDropTarget macro


## -description


Redraws a specified tree-view control item in the style used to indicate the target of a drag-and-drop operation. You can use this macro or the <a href="https://msdn.microsoft.com/en-us/library/Bb773901(v=VS.85).aspx">TreeView_Select</a> macro, or you can send the <a href="https://msdn.microsoft.com/en-us/library/Bb773736(v=VS.85).aspx">TVM_SELECTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item. 


## -remarks



If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="https://msdn.microsoft.com/en-us/library/Bb773537(v=VS.85).aspx">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb773533(v=VS.85).aspx">TVN_ITEMEXPANDED</a> notification codes. 

Using the <b>TreeView_SelectDropTarget</b> macro is equivalent to sending the <a href="https://msdn.microsoft.com/en-us/library/Bb773736(v=VS.85).aspx">TVM_SELECTITEM</a> message with its 
				<i>flag</i> parameter set to the TVGN_DROPHILITE value. 



