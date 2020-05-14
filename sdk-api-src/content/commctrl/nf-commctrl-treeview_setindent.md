---
UID: NF:commctrl.TreeView_SetIndent
title: TreeView_SetIndent macro (commctrl.h)
description: Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can use this macro or send the TVM_SETINDENT message explicitly.helpviewer_keywords: ["TreeView_SetIndent","TreeView_SetIndent macro [Windows Controls]","_win32_TreeView_SetIndent","_win32_TreeView_SetIndent_cpp","commctrl/TreeView_SetIndent","controls.TreeView_SetIndent","controls._win32_TreeView_SetIndent"]
old-location: controls\TreeView_SetIndent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setindent.htm
ms.date: 12/05/2018
ms.keywords: TreeView_SetIndent, TreeView_SetIndent macro [Windows Controls], _win32_TreeView_SetIndent, _win32_TreeView_SetIndent_cpp, commctrl/TreeView_SetIndent, controls.TreeView_SetIndent, controls._win32_TreeView_SetIndent
f1_keywords:
- commctrl/TreeView_SetIndent
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
- TreeView_SetIndent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_SetIndent macro


## -description


Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-setindent">TVM_SETINDENT</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param indent

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

Width, in pixels, of the indentation. If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum. 


## -remarks



The system-defined minimum indent value is typically five pixels, but it is not fixed. To retrieve the exact value of the minimum indent on a particular system, use the <b>TreeView_SetIndent</b> macro with <i>indent</i> set to zero. Then use the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_getindent">TreeView_GetIndent</a> macro to retrieve the minimum indent value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-setindent">TVM_SETINDENT</a>
 

 

