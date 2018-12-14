---
UID: NF:commctrl.TreeView_SetCheckState
title: TreeView_SetCheckState macro
author: windows-sdk-content
description: Sets the item's state image to &#0034;checked&#0034; or &#0034;unchecked.&#0034; You can also use the TVM_SETITEM message directly.
old-location: controls\TreeView_SetCheckState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setcheckstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TreeView_SetCheckState, TreeView_SetCheckState macro [Windows Controls], _win32_TreeView_SetCheckState, _win32_TreeView_SetCheckState_cpp, commctrl/TreeView_SetCheckState, controls.TreeView_SetCheckState, controls._win32_TreeView_SetCheckState
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
 - TreeView_SetCheckState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetCheckState macro


## -description


Sets the item's state image to "checked" or "unchecked." You can also use the <a href="https://msdn.microsoft.com/en-us/library/Bb773758(v=VS.85).aspx">TVM_SETITEM</a> message directly.


## -parameters




### -param hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hti

Type: <b>HTREEITEM</b>

Handle to the item. 


### -param fCheck

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value that indicates which state image is displayed. Set 
					<i>fCheck</i> to <b>TRUE</b> to display the checked state image or <b>FALSE</b> to display the unchecked image. 


## -remarks



A tree-view control can have two image lists. The normal image list stores the selected, nonselected, and overlay images. Check boxes are stored in the state image list and displayed to the left of the corresponding normal image. State images are specified by a one-based index. An index of zero indicates that there is no state image. See <a href="https://msdn.microsoft.com/en-us/library/Bb760017(v=VS.85).aspx">Tree-View Image Lists</a> for a discussion of how to handle tree-view images.

If you want to define your own state images, this macro assumes that the checked and unchecked images have the same indexes as the standard image list: 1 for unchecked and 2 for checked.



