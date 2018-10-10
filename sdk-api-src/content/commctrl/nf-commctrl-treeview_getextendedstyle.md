---
UID: NF:commctrl.TreeView_GetExtendedStyle
title: TreeView_GetExtendedStyle macro
author: windows-sdk-content
description: Retrieves the extended style for a specified tree-view control. Use this macro or send the TVM_GETEXTENDEDSTYLE message explicitly.
old-location: controls\TreeView_GetExtendedStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getextendedstyle.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TreeView_GetExtendedStyle, TreeView_GetExtendedStyle macro [Windows Controls], _shell_TreeView_GetExtendedStyle, _shell_TreeView_GetExtendedStyle_cpp, commctrl/TreeView_GetExtendedStyle, controls.TreeView_GetExtendedStyle, controls._shell_TreeView_GetExtendedStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - TreeView_GetExtendedStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetExtendedStyle macro


## -description


Retrieves the extended style for a specified tree-view control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773580(v=VS.85).aspx">TVM_GETEXTENDEDSTYLE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The extended styles for a tree-view control have nothing to do with the extended styles used with function <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> or function <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a>.
      



