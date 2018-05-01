---
UID: NF:commctrl.TreeView_SetLineColor
title: TreeView_SetLineColor macro
author: windows-driver-content
description: Sets the current line color. You can also use the TVM_SETLINECOLOR message directly.
old-location: controls\TreeView_SetLineColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setlinecolor.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_SetLineColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetLineColor macro


## -description


Sets the current line color. You can also use the <a href="https://msdn.microsoft.com/c5fc28af-5603-489f-aa6b-73e153f9aebc">TVM_SETLINECOLOR</a> message directly. 


## -parameters




### -param hwnd

TBD


### -param clr

TBD






#### - clrLine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that specifies the new line color. Use the CLR_DEFAULT value to restore the system default colors. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



This message only changes line colors. To change the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="https://msdn.microsoft.com/7aacaf9f-2bec-4f5e-84eb-0d51252f0247">TreeView_SetTextColor</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/c5fc28af-5603-489f-aa6b-73e153f9aebc">TVM_SETLINECOLOR</a>
 

 

