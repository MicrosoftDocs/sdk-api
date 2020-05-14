---
UID: NF:commctrl.TreeView_EndEditLabelNow
title: TreeView_EndEditLabelNow macro (commctrl.h)
description: Ends the editing of a tree-view item's label. You can use this macro or send the TVM_ENDEDITLABELNOW message explicitly.helpviewer_keywords: ["TreeView_EndEditLabelNow","TreeView_EndEditLabelNow macro [Windows Controls]","_win32_TreeView_EndEditLabelNow","_win32_TreeView_EndEditLabelNow_cpp","commctrl/TreeView_EndEditLabelNow","controls.TreeView_EndEditLabelNow","controls._win32_TreeView_EndEditLabelNow"]
old-location: controls\TreeView_EndEditLabelNow.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_endeditlabelnow.htm
ms.date: 12/05/2018
ms.keywords: TreeView_EndEditLabelNow, TreeView_EndEditLabelNow macro [Windows Controls], _win32_TreeView_EndEditLabelNow, _win32_TreeView_EndEditLabelNow_cpp, commctrl/TreeView_EndEditLabelNow, controls.TreeView_EndEditLabelNow, controls._win32_TreeView_EndEditLabelNow
f1_keywords:
- commctrl/TreeView_EndEditLabelNow
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
- TreeView_EndEditLabelNow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_EndEditLabelNow macro


## -description


Ends the editing of a tree-view item's label. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-endeditlabelnow">TVM_ENDEDITLABELNOW</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param fCancel

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Variable that indicates whether the editing is canceled without being saved to the label. If this parameter is <b>TRUE</b>, the system cancels editing without saving the changes. Otherwise, the system saves the changes to the label. 


## -remarks



This macro causes the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-endlabeledit">TVN_ENDLABELEDIT</a> notification code to be sent to the parent window of the tree-view control. 



