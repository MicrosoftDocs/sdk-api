---
UID: NF:commctrl.TreeView_SetTextColor
title: TreeView_SetTextColor macro (commctrl.h)
author: windows-sdk-content
description: Sets the text color of the control. You can use this macro or send the TVM_SETTEXTCOLOR message explicitly.
old-location: controls\TreeView_SetTextColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_settextcolor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TreeView_SetTextColor, TreeView_SetTextColor macro [Windows Controls], _win32_TreeView_SetTextColor, _win32_TreeView_SetTextColor_cpp, commctrl/TreeView_SetTextColor, controls.TreeView_SetTextColor, controls._win32_TreeView_SetTextColor
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
 - TreeView_SetTextColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetTextColor macro


## -description


Sets the text color of the control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773769(v=VS.85).aspx">TVM_SETTEXTCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


### -param clr

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that contains the new text color. If this argument is -1, the control will revert to using the system color for the text color. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773893(v=VS.85).aspx">TreeView_GetTextColor</a>
 

 

