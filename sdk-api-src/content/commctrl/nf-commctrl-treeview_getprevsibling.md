---
UID: NF:commctrl.TreeView_GetPrevSibling
title: TreeView_GetPrevSibling macro
author: windows-driver-content
description: Retrieves the previous sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_PREVIOUS flag.
old-location: controls\TreeView_GetPrevSibling.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getprevsibling.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TreeView_GetPrevSibling
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetPrevSibling macro


## -description


Retrieves the previous sibling item of a specified item in a tree-view control. You can use this macro, or you can explicitly send the <a href="https://msdn.microsoft.com/505c713c-7728-4119-bc0e-482fe7e73193">TVM_GETNEXTITEM</a> message with the TVGN_PREVIOUS flag. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/49eb25c4-52b3-4b3a-ae2f-433af9adf0d4">TreeView_GetChild</a>



<a href="https://msdn.microsoft.com/987d0d0f-eecf-4a6a-9340-64dd6ce1ac80">TreeView_GetNextItem</a>



<a href="https://msdn.microsoft.com/1fe480ea-dcb5-4d08-8eec-996f78757fda">TreeView_GetNextSibling</a>



<a href="https://msdn.microsoft.com/a286e32f-d152-4cd9-b7fc-75d946378c34">TreeView_GetParent</a>
 

 

