---
UID: NF:commctrl.TreeView_GetEditControl
title: TreeView_GetEditControl macro
author: windows-sdk-content
description: Retrieves the handle to the edit control being used to edit a tree-view item's text. You can use this macro or send the TVM_GETEDITCONTROL message explicitly.
old-location: controls\TreeView_GetEditControl.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_geteditcontrol.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: TreeView_GetEditControl, TreeView_GetEditControl macro [Windows Controls], _win32_TreeView_GetEditControl, _win32_TreeView_GetEditControl_cpp, commctrl/TreeView_GetEditControl, controls.TreeView_GetEditControl, controls._win32_TreeView_GetEditControl
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
 - TreeView_GetEditControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetEditControl macro


## -description


Retrieves the handle to the edit control being used to edit a tree-view item's text. You can use this macro or send the <a href="https://msdn.microsoft.com/c89e57e8-e113-47a1-85e6-bb68990f9c1a">TVM_GETEDITCONTROL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



When label editing begins, an edit control is created but not positioned or displayed. Before it is displayed, the tree-view control sends its parent window a <a href="https://msdn.microsoft.com/67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44">TVN_BEGINLABELEDIT</a> notification code. 

To customize label editing, implement a handler for <a href="https://msdn.microsoft.com/67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44">TVN_BEGINLABELEDIT</a> and have it use <b>TreeView_GetEditControl</b> to send a <a href="https://msdn.microsoft.com/c89e57e8-e113-47a1-85e6-bb68990f9c1a">TVM_GETEDITCONTROL</a> message to the tree-view control. If a label is being edited, the return value will be a handle to the edit control. Use this handle to customize the edit control by sending the usual EM_XXX messages. 



