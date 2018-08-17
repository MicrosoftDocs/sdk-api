---
UID: NF:commctrl.TreeView_GetScrollTime
title: TreeView_GetScrollTime macro
author: windows-sdk-content
description: Retrieves the maximum scroll time for the tree-view control. You can use this macro or send the TVM_GETSCROLLTIME message explicitly.
old-location: controls\TreeView_GetScrollTime.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getscrolltime.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TreeView_GetScrollTime, TreeView_GetScrollTime macro [Windows Controls], _win32_TreeView_GetScrollTime, _win32_TreeView_GetScrollTime_cpp, commctrl/TreeView_GetScrollTime, controls.TreeView_GetScrollTime, controls._win32_TreeView_GetScrollTime
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
 - TreeView_GetScrollTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetScrollTime macro


## -description


Retrieves the maximum scroll time for the tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773625(v=VS.85).aspx">TVM_GETSCROLLTIME</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The maximum scroll time is the longest amount of time that a scroll operation can take. Scrolling will be adjusted so that the scroll will take place within the maximum scroll time. A scroll operation may take less time than the maximum. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760129(v=VS.85).aspx">TreeView_SetScrollTime</a>
 

 

