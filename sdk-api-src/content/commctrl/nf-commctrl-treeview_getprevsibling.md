---
UID: NF:commctrl.TreeView_GetPrevSibling
title: TreeView_GetPrevSibling macro
author: windows-sdk-content
description: Retrieves the previous sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PREVIOUS flag.
old-location: controls\TreeView_GetPrevSibling.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getprevsibling.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TreeView_GetPrevSibling, TreeView_GetPrevSibling macro [Windows Controls], _win32_TreeView_GetPrevSibling, _win32_TreeView_GetPrevSibling_cpp, commctrl/TreeView_GetPrevSibling, controls.TreeView_GetPrevSibling, controls._win32_TreeView_GetPrevSibling
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
 - TreeView_GetPrevSibling
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_GetPrevSibling macro


## -description


Retrieves the previous sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/en-us/library/Bb773622(v=VS.85).aspx">TVM_GETNEXTITEM</a> message with the TVGN_PREVIOUS flag. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773812(v=VS.85).aspx">TreeView_GetChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773861(v=VS.85).aspx">TreeView_GetNextItem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773867(v=VS.85).aspx">TreeView_GetNextSibling</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773872(v=VS.85).aspx">TreeView_GetParent</a>
 

 

