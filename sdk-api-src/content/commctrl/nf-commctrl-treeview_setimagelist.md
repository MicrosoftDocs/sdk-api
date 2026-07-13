---
UID: NF:commctrl.TreeView_SetImageList
title: TreeView_SetImageList macro (commctrl.h)
description: Sets the normal or state image list for a tree-view control and redraws the control using the new images. You can use this macro or send the TVM_SETIMAGELIST message explicitly.
helpviewer_keywords: ["TVSIL_NORMAL","TVSIL_STATE","TreeView_SetImageList","TreeView_SetImageList macro [Windows Controls]","_win32_TreeView_SetImageList","_win32_TreeView_SetImageList_cpp","commctrl/TreeView_SetImageList","controls.TreeView_SetImageList","controls._win32_TreeView_SetImageList"]
old-location: controls\TreeView_SetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setimagelist.htm
ms.date: 10/21/2024
ms.keywords: TVSIL_NORMAL, TVSIL_STATE, TreeView_SetImageList, TreeView_SetImageList macro [Windows Controls], _win32_TreeView_SetImageList, _win32_TreeView_SetImageList_cpp, commctrl/TreeView_SetImageList, controls.TreeView_SetImageList, controls._win32_TreeView_SetImageList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TreeView_SetImageList
 - commctrl/TreeView_SetImageList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_SetImageList
---

# TreeView_SetImageList macro

## -syntax

```cpp
HIMAGELIST TreeView_SetImageList(
   HWND       hwnd,
   HIMAGELIST himl,
   INT        iImage
);
```

## -returns

Type: **HIMAGELIST**

Returns the HIMAGELIST handle to the previous image list, if any, or <b>NULL</b> otherwise.


## -description

Sets the normal or state image list for a tree-view control and redraws the control using the new images. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setimagelist">TVM_SETIMAGELIST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param himl

Type: <b>HIMAGELIST</b>

The HIMAGELIST handle to the image list. If <i>himl</i> is <b>NULL</b>, the message removes the specified image list from the tree-view control.

### -param iImage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

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



<a href="/windows/desktop/Controls/tvm-getimagelist">TVM_GETIMAGELIST</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getimagelist">TreeView_GetImageList</a>
