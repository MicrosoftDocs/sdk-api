---
UID: NF:commctrl.TreeView_SelectSetFirstVisible
title: TreeView_SelectSetFirstVisible macro
author: windows-sdk-content
description: Scrolls the tree-view control vertically to ensure that the specified item is visible.
old-location: controls\TreeView_SelectSetFirstVisible.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_selectsetfirstvisible.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TreeView_SelectSetFirstVisible, TreeView_SelectSetFirstVisible macro [Windows Controls], _win32_TreeView_SelectSetFirstVisible, _win32_TreeView_SelectSetFirstVisible_cpp, commctrl/TreeView_SelectSetFirstVisible, controls.TreeView_SelectSetFirstVisible, controls._win32_TreeView_SelectSetFirstVisible
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
 - TreeView_SelectSetFirstVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SelectSetFirstVisible macro


## -description


Scrolls the tree-view control vertically to ensure that the specified item is visible. If possible, the specified item becomes the first visible item at the top of the control's window. You can use this macro or the <a href="https://msdn.microsoft.com/en-us/library/Bb773901(v=VS.85).aspx">TreeView_Select</a> macro, or you can send the <a href="https://msdn.microsoft.com/en-us/library/Bb773736(v=VS.85).aspx">TVM_SELECTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item. 


## -remarks



Tree-view controls display as many items as will fit in the window. If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window. 

If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="https://msdn.microsoft.com/en-us/library/Bb773537(v=VS.85).aspx">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb773533(v=VS.85).aspx">TVN_ITEMEXPANDED</a> notification codes. 

Using the <b>TreeView_SelectSetFirstVisible</b> macro is equivalent to sending the <a href="https://msdn.microsoft.com/en-us/library/Bb773736(v=VS.85).aspx">TVM_SELECTITEM</a> message with its <i>flag</i> parameter set to the TVGN_FIRSTVISIBLE value. 



