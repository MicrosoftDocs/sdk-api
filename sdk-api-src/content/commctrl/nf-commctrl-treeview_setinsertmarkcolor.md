---
UID: NF:commctrl.TreeView_SetInsertMarkColor
title: TreeView_SetInsertMarkColor macro
author: windows-sdk-content
description: Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the TVM_SETINSERTMARKCOLOR message explicitly.
old-location: controls\TreeView_SetInsertMarkColor.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setinsertmarkcolor.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeView_SetInsertMarkColor, TreeView_SetInsertMarkColor macro [Windows Controls], _win32_TreeView_SetInsertMarkColor, _win32_TreeView_SetInsertMarkColor_cpp, commctrl/TreeView_SetInsertMarkColor, controls.TreeView_SetInsertMarkColor, controls._win32_TreeView_SetInsertMarkColor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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


Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773755(v=VS.85).aspx">TVM_SETINSERTMARKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to a tree-view control. 


### -param clr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Dd183449(v=VS.85).aspx">COLORREF</a> value that contains the new insertion mark color. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773835(v=VS.85).aspx">TreeView_GetInsertMarkColor</a>
 

 

