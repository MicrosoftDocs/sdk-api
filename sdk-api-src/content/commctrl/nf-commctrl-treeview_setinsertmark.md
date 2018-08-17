---
UID: NF:commctrl.TreeView_SetInsertMark
title: TreeView_SetInsertMark macro
author: windows-sdk-content
description: Sets the insertion mark in a tree-view control. You can use this macro or send the TVM_SETINSERTMARK message explicitly.
old-location: controls\TreeView_SetInsertMark.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setinsertmark.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeView_SetInsertMark, TreeView_SetInsertMark macro [Windows Controls], _win32_TreeView_SetInsertMark, _win32_TreeView_SetInsertMark_cpp, commctrl/TreeView_SetInsertMark, controls.TreeView_SetInsertMark, controls._win32_TreeView_SetInsertMark
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
 - TreeView_SetInsertMark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetInsertMark macro


## -description


Sets the insertion mark in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/35441807-406a-408c-ad89-6dd40c907e3c">TVM_SETINSERTMARK</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


### -param hItem

Type: <b>HTREEITEM</b>

<b>HTREEITEM</b> that specifies at which item the insertion mark will be placed. If this argument is <b>NULL</b>, the insertion mark is removed. 


### -param fAfter

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>BOOL</b> value that specifies if the insertion mark is placed before or after the specified item. If this argument is nonzero, the insertion mark will be placed after the item. If this argument is zero, the insertion mark will be placed before the item. 

