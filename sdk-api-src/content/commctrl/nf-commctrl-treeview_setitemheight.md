---
UID: NF:commctrl.TreeView_SetItemHeight
title: TreeView_SetItemHeight macro
author: windows-sdk-content
description: Sets the height of the tree-view items. You can use this macro or send the TVM_SETITEMHEIGHT message explicitly.
old-location: controls\TreeView_SetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setitemheight.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TreeView_SetItemHeight, TreeView_SetItemHeight macro [Windows Controls], _win32_TreeView_SetItemHeight, _win32_TreeView_SetItemHeight_cpp, commctrl/TreeView_SetItemHeight, controls.TreeView_SetItemHeight, controls._win32_TreeView_SetItemHeight
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
 - TreeView_SetItemHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetItemHeight macro


## -description


Sets the height of the tree-view items. You can use this macro or send the <a href="https://msdn.microsoft.com/23f6f2a4-cdd9-441d-af24-ed40513d2721">TVM_SETITEMHEIGHT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


### -param iHeight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

New height of every item in the tree view, in pixels. Heights less than 1 will be set to 1. If this argument is not even, it will be rounded down to the nearest even value. If this argument is -1, the control will revert to using its default item height. 


## -remarks



The tree-view control uses this value for the height of all items. To modify the height of individual items, see the description of the <b>iIntegral</b> member of the <a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a> structure. 




## -see-also




<a href="https://msdn.microsoft.com/ca9d9a48-702d-4ea5-b3e3-bb9b71ca9518">TreeView_GetItemHeight</a>
 

 

