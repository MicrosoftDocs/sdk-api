---
UID: NF:commctrl.TreeView_GetScrollTime
title: TreeView_GetScrollTime macro
author: windows-driver-content
description: Retrieves the maximum scroll time for the tree-view control. You can use this macro or send the TVM_GETSCROLLTIME message explicitly.
old-location: controls\TreeView_GetScrollTime.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getscrolltime.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: TreeView_GetScrollTime, TreeView_GetScrollTime macro [Windows Controls], _win32_TreeView_GetScrollTime, _win32_TreeView_GetScrollTime_cpp, commctrl/TreeView_GetScrollTime, controls.TreeView_GetScrollTime, controls._win32_TreeView_GetScrollTime
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
-	TreeView_GetScrollTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetScrollTime macro


## -description


Retrieves the maximum scroll time for the tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/992d1906-cda3-4ac7-ba90-c681c551ac2e">TVM_GETSCROLLTIME</a> message explicitly. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The maximum scroll time is the longest amount of time that a scroll operation can take. Scrolling will be adjusted so that the scroll will take place within the maximum scroll time. A scroll operation may take less time than the maximum. 




## -see-also




<a href="https://msdn.microsoft.com/3f7705d6-22bb-4fe6-a001-da95b9b29197">TreeView_SetScrollTime</a>
 

 

