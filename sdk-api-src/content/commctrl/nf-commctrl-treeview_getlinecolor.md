---
UID: NF:commctrl.TreeView_GetLineColor
title: TreeView_GetLineColor macro
author: windows-driver-content
description: Gets the current line color. You can also use the TVM_GETLINECOLOR message directly.
old-location: controls\TreeView_GetLineColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getlinecolor.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: TreeView_GetLineColor, TreeView_GetLineColor macro [Windows Controls], _win32_TreeView_GetLineColor, _win32_TreeView_GetLineColor_cpp, commctrl/TreeView_GetLineColor, controls.TreeView_GetLineColor, controls._win32_TreeView_GetLineColor
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_GetLineColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetLineColor macro


## -description


Gets the current line color. You can also use the <a href="https://msdn.microsoft.com/e74441b3-5d4f-4454-b896-2e96ce649419">TVM_GETLINECOLOR</a> message directly. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



This message only retrieves line colors. To retrieve the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="https://msdn.microsoft.com/a4c003eb-0e0e-496a-a048-ce733e8fcd45">TreeView_GetTextColor</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/e74441b3-5d4f-4454-b896-2e96ce649419">TVM_GETLINECOLOR</a>
 

 

