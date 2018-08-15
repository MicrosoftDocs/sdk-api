---
UID: NF:commctrl.TreeView_SetImageList
title: TreeView_SetImageList macro
author: windows-sdk-content
description: Sets the normal or state image list for a tree-view control and redraws the control using the new images. You can use this macro or send the TVM_SETIMAGELIST message explicitly.
old-location: controls\TreeView_SetImageList.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setimagelist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TVSIL_NORMAL, TVSIL_STATE, TreeView_SetImageList, TreeView_SetImageList macro [Windows Controls], _win32_TreeView_SetImageList, _win32_TreeView_SetImageList_cpp, commctrl/TreeView_SetImageList, controls.TreeView_SetImageList, controls._win32_TreeView_SetImageList
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
 - TreeView_SetImageList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetImageList macro


## -description


Sets the normal or state image list for a tree-view control and redraws the control using the new images. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773747(v=VS.85).aspx">TVM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param himl

Type: <b>HIMAGELIST</b>

The HIMAGELIST handle to the image list. If <i>himl</i> is <b>NULL</b>, the message removes the specified image list from the tree-view control. 


### -param iImage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Type of image list to set. This parameter can be one of the following values: 

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
 


## -remarks



The tree-view control will not destroy the image list specified with this message. Your application must destroy the image list when it is no longer needed. 




## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773585(v=VS.85).aspx">TVM_GETIMAGELIST</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773829(v=VS.85).aspx">TreeView_GetImageList</a>
 

 

