---
UID: NF:commctrl.TreeView_SetInsertMarkColor
title: TreeView_SetInsertMarkColor macro (commctrl.h)
description: Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the TVM_SETINSERTMARKCOLOR message explicitly.
helpviewer_keywords: ["TreeView_SetInsertMarkColor","TreeView_SetInsertMarkColor macro [Windows Controls]","_win32_TreeView_SetInsertMarkColor","_win32_TreeView_SetInsertMarkColor_cpp","commctrl/TreeView_SetInsertMarkColor","controls.TreeView_SetInsertMarkColor","controls._win32_TreeView_SetInsertMarkColor"]
old-location: controls\TreeView_SetInsertMarkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setinsertmarkcolor.htm
ms.date: 12/05/2018
ms.keywords: TreeView_SetInsertMarkColor, TreeView_SetInsertMarkColor macro [Windows Controls], _win32_TreeView_SetInsertMarkColor, _win32_TreeView_SetInsertMarkColor_cpp, commctrl/TreeView_SetInsertMarkColor, controls.TreeView_SetInsertMarkColor, controls._win32_TreeView_SetInsertMarkColor
f1_keywords:
- commctrl/TreeView_SetInsertMarkColor
dev_langs:
- c++
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
- TreeView_SetInsertMarkColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_SetInsertMarkColor macro


## -description


Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-setinsertmarkcolor">TVM_SETINSERTMARKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control. 


### -param clr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value that contains the new insertion mark color. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getinsertmarkcolor">TreeView_GetInsertMarkColor</a>
 

 

