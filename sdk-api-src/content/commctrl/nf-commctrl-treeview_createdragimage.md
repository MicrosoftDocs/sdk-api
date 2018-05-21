---
UID: NF:commctrl.TreeView_CreateDragImage
title: TreeView_CreateDragImage macro
author: windows-driver-content
description: Creates a dragging bitmap for the specified item in a tree-view control.
old-location: controls\TreeView_CreateDragImage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_createdragimage.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: TreeView_CreateDragImage, TreeView_CreateDragImage macro [Windows Controls], _win32_TreeView_CreateDragImage, _win32_TreeView_CreateDragImage_cpp, commctrl/TreeView_CreateDragImage, controls.TreeView_CreateDragImage, controls._win32_TreeView_CreateDragImage
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
-	TreeView_CreateDragImage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_CreateDragImage macro


## -description


Creates a dragging bitmap for the specified item in a tree-view control. The macro also creates an image list for the bitmap and adds the bitmap to the image list. An application can display the image when dragging the item by using the image list functions. You can use this macro or send the <a href="https://msdn.microsoft.com/fbe97921-c9d3-473c-933c-d6bc0599e24d">TVM_CREATEDRAGIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the item that receives the new dragging bitmap. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



If you create a tree-view control without an associated image list, you cannot use the <b>TreeView_CreateDragImage</b> macro to create the image to display during a drag operation. You must implement your own method of creating a drag cursor.

Your application is responsible for destroying the image list when it is no longer needed.



