---
UID: NF:commctrl.TreeView_SetLineColor
title: TreeView_SetLineColor macro
author: windows-sdk-content
description: Sets the current line color. You can also use the TVM_SETLINECOLOR message directly.
old-location: controls\TreeView_SetLineColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setlinecolor.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TreeView_SetLineColor, TreeView_SetLineColor macro [Windows Controls], _win32_TreeView_SetLineColor, _win32_TreeView_SetLineColor_cpp, commctrl/TreeView_SetLineColor, controls.TreeView_SetLineColor, controls._win32_TreeView_SetLineColor
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
 - TreeView_SetLineColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetLineColor macro


## -description


Sets the current line color. You can also use the <a href="https://msdn.microsoft.com/en-us/library/Bb773764(v=VS.85).aspx">TVM_SETLINECOLOR</a> message directly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


### -param clr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Dd183449(v=VS.85).aspx">COLORREF</a> that specifies the new line color. Use the CLR_DEFAULT value to restore the system default colors. 


## -remarks



This message only changes line colors. To change the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="https://msdn.microsoft.com/en-us/library/Bb760131(v=VS.85).aspx">TreeView_SetTextColor</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773764(v=VS.85).aspx">TVM_SETLINECOLOR</a>
 

 

