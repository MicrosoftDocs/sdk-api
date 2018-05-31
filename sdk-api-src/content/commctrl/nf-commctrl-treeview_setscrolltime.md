---
UID: NF:commctrl.TreeView_SetScrollTime
title: TreeView_SetScrollTime macro
author: windows-sdk-content
description: Sets the maximum scroll time for the tree-view control. You can use this macro or send the TVM_SETSCROLLTIME message explicitly.
old-location: controls\TreeView_SetScrollTime.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setscrolltime.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: TreeView_SetScrollTime, TreeView_SetScrollTime macro [Windows Controls], _win32_TreeView_SetScrollTime, _win32_TreeView_SetScrollTime_cpp, commctrl/TreeView_SetScrollTime, controls.TreeView_SetScrollTime, controls._win32_TreeView_SetScrollTime
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_SetScrollTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetScrollTime macro


## -description


Sets the maximum scroll time for the tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a">TVM_SETSCROLLTIME</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param uTime

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


#### - uMaxScrollTime

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

New maximum scroll time, in milliseconds. If this value is less than 100, it will be rounded up to 100. 


## -remarks



The maximum scroll time is the longest amount of time that a scroll operation can take. Scrolling will be adjusted so that the scroll will take place within the maximum scroll time. A scroll operation may take less time than the maximum.




## -see-also




<a href="https://msdn.microsoft.com/992d1906-cda3-4ac7-ba90-c681c551ac2e">TVM_GETSCROLLTIME</a>
 

 

