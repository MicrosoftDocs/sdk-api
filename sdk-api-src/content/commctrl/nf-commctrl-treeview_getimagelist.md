---
UID: NF:commctrl.TreeView_GetImageList
title: TreeView_GetImageList macro (commctrl.h)
description: Retrieves the handle to the normal or state image list associated with a tree-view control. You can use this macro or send the TVM_GETIMAGELIST message explicitly.helpviewer_keywords: ["TVSIL_NORMAL","TVSIL_STATE","TreeView_GetImageList","TreeView_GetImageList macro [Windows Controls]","_win32_TreeView_GetImageList","_win32_TreeView_GetImageList_cpp","commctrl/TreeView_GetImageList","controls.TreeView_GetImageList","controls._win32_TreeView_GetImageList"]
old-location: controls\TreeView_GetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getimagelist.htm
ms.date: 12/05/2018
ms.keywords: TVSIL_NORMAL, TVSIL_STATE, TreeView_GetImageList, TreeView_GetImageList macro [Windows Controls], _win32_TreeView_GetImageList, _win32_TreeView_GetImageList_cpp, commctrl/TreeView_GetImageList, controls.TreeView_GetImageList, controls._win32_TreeView_GetImageList
f1_keywords:
- commctrl/TreeView_GetImageList
dev_langs:
- c++
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
- TreeView_GetImageList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_GetImageList macro


## -description


Retrieves the handle to the normal or state image list associated with a tree-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-getimagelist">TVM_GETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control. 


### -param iImage

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

Type of image list to retrieve. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVSIL_NORMAL"></a><a id="tvsil_normal"></a><dl>
<dt><b>TVSIL_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.

</td>
</tr>
<tr>
<td width="40%"><a id="TVSIL_STATE"></a><a id="tvsil_state"></a><dl>
<dt><b>TVSIL_STATE</b></dt>
</dl>
</td>
<td width="60%">
Indicates the state image list. You can use state images to indicate application-defined item states. A state image is displayed to the left of an item's selected or nonselected image. 

</td>
</tr>
</table>
 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-treeview_setimagelist">TreeView_SetImageList</a>
 

 

