---
UID: NF:commctrl.TreeView_GetExtendedStyle
title: TreeView_GetExtendedStyle macro (commctrl.h)
description: Retrieves the extended style for a specified tree-view control. Use this macro or send the TVM_GETEXTENDEDSTYLE message explicitly.
old-location: controls\TreeView_GetExtendedStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getextendedstyle.htm
ms.date: 12/05/2018
ms.keywords: TreeView_GetExtendedStyle, TreeView_GetExtendedStyle macro [Windows Controls], _shell_TreeView_GetExtendedStyle, _shell_TreeView_GetExtendedStyle_cpp, commctrl/TreeView_GetExtendedStyle, controls.TreeView_GetExtendedStyle, controls._shell_TreeView_GetExtendedStyle
f1_keywords:
- commctrl/TreeView_GetExtendedStyle
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- TreeView_GetExtendedStyle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetExtendedStyle macro


## -description


Retrieves the extended style for a specified tree-view control. Use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getextendedstyle">TVM_GETEXTENDEDSTYLE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The extended styles for a tree-view control have nothing to do with the extended styles used with function <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> or function <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>.
      



