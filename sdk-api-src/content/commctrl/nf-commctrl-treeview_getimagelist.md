---
UID: NF:commctrl.TreeView_GetImageList
title: TreeView_GetImageList macro
author: windows-sdk-content
description: Retrieves the handle to the normal or state image list associated with a tree-view control. You can use this macro or send the TVM_GETIMAGELIST message explicitly.
old-location: controls\TreeView_GetImageList.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getimagelist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TVSIL_NORMAL, TVSIL_STATE, TreeView_GetImageList, TreeView_GetImageList macro [Windows Controls], _win32_TreeView_GetImageList, _win32_TreeView_GetImageList_cpp, commctrl/TreeView_GetImageList, controls.TreeView_GetImageList, controls._win32_TreeView_GetImageList
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
 - TreeView_GetImageList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetImageList macro


## -description


Retrieves the handle to the normal or state image list associated with a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773585(v=VS.85).aspx">TVM_GETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tree-view control. 


### -param iImage

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">INT</a></b>

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




<a href="https://msdn.microsoft.com/en-us/library/Bb760056(v=VS.85).aspx">TreeView_SetImageList</a>
 

 

