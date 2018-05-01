---
UID: NF:commctrl.TreeView_GetImageList
title: TreeView_GetImageList macro
author: windows-driver-content
description: Retrieves the handle to the normal or state image list associated with a tree-view control. You can use this macro or send the TVM_GETIMAGELIST message explicitly.
old-location: controls\TreeView_GetImageList.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getimagelist.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: TVSIL_NORMAL, TVSIL_STATE, TreeView_GetImageList, TreeView_GetImageList macro [Windows Controls], _win32_TreeView_GetImageList, _win32_TreeView_GetImageList_cpp, commctrl/TreeView_GetImageList, controls.TreeView_GetImageList, controls._win32_TreeView_GetImageList
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
-	TreeView_GetImageList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_GetImageList macro


## -description


Retrieves the handle to the normal or state image list associated with a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/bcf5eac8-cb07-4cf8-ad93-47319fc915a5">TVM_GETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iImage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

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
 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<a href="https://msdn.microsoft.com/72748b47-0797-4607-8c0b-ba88d2f20c24">TreeView_SetImageList</a>
 

 

