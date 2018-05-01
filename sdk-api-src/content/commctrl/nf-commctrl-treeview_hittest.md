---
UID: NF:commctrl.TreeView_HitTest
title: TreeView_HitTest macro
author: windows-driver-content
description: Determines the location of the specified point relative to the client area of a tree-view control. You can use this macro or send the TVM_HITTEST message explicitly.
old-location: controls\TreeView_HitTest.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_hittest.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: TreeView_HitTest, TreeView_HitTest macro [Windows Controls], _win32_TreeView_HitTest, _win32_TreeView_HitTest_cpp, commctrl/TreeView_HitTest, controls.TreeView_HitTest, controls._win32_TreeView_HitTest
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
-	TreeView_HitTest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_HitTest macro


## -description


Determines the location of the specified point relative to the client area of a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/18ea3737-f429-4c10-9133-3b5729aa36fa">TVM_HITTEST</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param lpht

Type: <b>LPTVHITTESTINFO</b>

Pointer to a <a href="https://msdn.microsoft.com/9df3106f-50bb-4f53-a498-6b2d31279424">TVHITTESTINFO</a> structure. When the message is sent, the <b>pt</b> member specifies the coordinates of the point to test. When the message returns, the <b>hItem</b> member is the handle to the item at the specified point or <b>NULL</b> if no item occupies the point. Also, when the message returns, the <b>flags</b> member is a hit test value that indicates the location of the specified point. For a list of hit test values, see the description of the <b>TVHITTESTINFO</b> structure. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 

