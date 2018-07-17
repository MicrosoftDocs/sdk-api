---
UID: NF:commctrl.TreeView_SetInsertMarkColor
title: TreeView_SetInsertMarkColor macro
author: windows-sdk-content
description: Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the TVM_SETINSERTMARKCOLOR message explicitly.
old-location: controls\TreeView_SetInsertMarkColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setinsertmarkcolor.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: TreeView_SetInsertMarkColor, TreeView_SetInsertMarkColor macro [Windows Controls], _win32_TreeView_SetInsertMarkColor, _win32_TreeView_SetInsertMarkColor_cpp, commctrl/TreeView_SetInsertMarkColor, controls.TreeView_SetInsertMarkColor, controls._win32_TreeView_SetInsertMarkColor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_SetInsertMarkColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetInsertMarkColor macro


## -description


Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the <a href="https://msdn.microsoft.com/c82304a8-3726-42c0-81e7-90d8f8205ead">TVM_SETINSERTMARKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param clr

TBD






#### - clrInsertMark

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that contains the new insertion mark color. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


## -see-also




<a href="https://msdn.microsoft.com/958ec5ff-9b6e-44de-940a-fbbb2e2857a8">TreeView_GetInsertMarkColor</a>
 

 

