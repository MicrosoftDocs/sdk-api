---
UID: NF:commctrl.TreeView_GetLineColor
title: TreeView_GetLineColor macro (commctrl.h)
description: Gets the current line color. You can also use the TVM_GETLINECOLOR message directly.helpviewer_keywords: ["TreeView_GetLineColor","TreeView_GetLineColor macro [Windows Controls]","_win32_TreeView_GetLineColor","_win32_TreeView_GetLineColor_cpp","commctrl/TreeView_GetLineColor","controls.TreeView_GetLineColor","controls._win32_TreeView_GetLineColor"]
old-location: controls\TreeView_GetLineColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getlinecolor.htm
ms.date: 12/05/2018
ms.keywords: TreeView_GetLineColor, TreeView_GetLineColor macro [Windows Controls], _win32_TreeView_GetLineColor, _win32_TreeView_GetLineColor_cpp, commctrl/TreeView_GetLineColor, controls.TreeView_GetLineColor, controls._win32_TreeView_GetLineColor
f1_keywords:
- commctrl/TreeView_GetLineColor
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
- TreeView_GetLineColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetLineColor macro


## -description


Gets the current line color. You can also use the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getlinecolor">TVM_GETLINECOLOR</a> message directly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


## -remarks



This message only retrieves line colors. To retrieve the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_gettextcolor">TreeView_GetTextColor</a> macro.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getlinecolor">TVM_GETLINECOLOR</a>
 

 

