---
UID: NF:commctrl.TreeView_SetIndent
title: TreeView_SetIndent macro
author: windows-sdk-content
description: Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can use this macro or send the TVM_SETINDENT message explicitly.
old-location: controls\TreeView_SetIndent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setindent.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TreeView_SetIndent, TreeView_SetIndent macro [Windows Controls], _win32_TreeView_SetIndent, _win32_TreeView_SetIndent_cpp, commctrl/TreeView_SetIndent, controls.TreeView_SetIndent, controls._win32_TreeView_SetIndent
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
 - TreeView_SetIndent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetIndent macro


## -description


Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773750(v=VS.85).aspx">TVM_SETINDENT</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


### -param indent

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">INT</a></b>

Width, in pixels, of the indentation. If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum. 


## -remarks



The system-defined minimum indent value is typically five pixels, but it is not fixed. To retrieve the exact value of the minimum indent on a particular system, use the <b>TreeView_SetIndent</b> macro with <i>indent</i> set to zero. Then use the <a href="https://msdn.microsoft.com/en-us/library/Bb773832(v=VS.85).aspx">TreeView_GetIndent</a> macro to retrieve the minimum indent value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773750(v=VS.85).aspx">TVM_SETINDENT</a>
 

 

