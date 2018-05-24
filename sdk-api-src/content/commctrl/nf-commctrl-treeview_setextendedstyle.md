---
UID: NF:commctrl.TreeView_SetExtendedStyle
title: TreeView_SetExtendedStyle macro
author: windows-driver-content
description: Sets the extended style for a specified TreeView control. Use this macro or send the TVM_SETEXTENDEDSTYLE message explicitly.
old-location: controls\TreeView_SetExtendedStyle.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setextendedstyle.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: TreeView_SetExtendedStyle, TreeView_SetExtendedStyle macro [Windows Controls], _shell_TreeView_SetExtendedStyle, _shell_TreeView_SetExtendedStyle_cpp, commctrl/TreeView_SetExtendedStyle, controls.TreeView_SetExtendedStyle, controls._shell_TreeView_SetExtendedStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	TreeView_SetExtendedStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_SetExtendedStyle macro


## -description


Sets the extended style for a specified TreeView control. Use this macro or send the <a href="https://msdn.microsoft.com/35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5">TVM_SETEXTENDEDSTYLE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the TreeView control.


### -param dw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Value that indicates the extended style. For more information on styles, see <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">Tree-View Control Extended Styles</a>.


### -param mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Mask used to select the styles to be set.

