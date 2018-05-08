---
UID: NF:commctrl.TreeView_SetToolTips
title: TreeView_SetToolTips macro
author: windows-driver-content
description: Sets a tree-view control's child tooltip control. You can use this macro or send the TVM_SETTOOLTIPS message explicitly.
old-location: controls\TreeView_SetToolTips.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_settooltips.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: TreeView_SetToolTips, TreeView_SetToolTips macro [Windows Controls], _win32_TreeView_SetToolTips, _win32_TreeView_SetToolTips_cpp, commctrl/TreeView_SetToolTips, controls.TreeView_SetToolTips, controls._win32_TreeView_SetToolTips
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_SetToolTips
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetToolTips macro


## -description


Sets a tree-view control's child tooltip control. You can use this macro or send the <a href="https://msdn.microsoft.com/beb9a739-868e-46a8-95d9-9dc032c79dd4">TVM_SETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hwndTT

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


#### - hwndTooltip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tooltip control. 


## -remarks



When created, tree-view controls automatically create a child tooltip control. To prevent a tree-view control from using tooltips, create the control with the <a href="Tree_View_Control_Window_Styles.htm">TVS_NOTOOLTIPS</a> style. 




## -see-also




<a href="https://msdn.microsoft.com/25d82a01-c376-4d08-9ee6-eef892bcf4a9">TreeView_GetToolTips</a>
 

 

