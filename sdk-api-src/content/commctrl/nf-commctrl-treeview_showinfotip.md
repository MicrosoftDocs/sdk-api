---
UID: NF:commctrl.TreeView_ShowInfoTip
title: TreeView_ShowInfoTip macro
author: windows-sdk-content
description: Shows the infotip for a specified item in a tree-view control. Use this macro or send the TVM_SHOWINFOTIP message explicitly.
old-location: controls\TreeView_ShowInfoTip.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_showinfotip.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TreeView_ShowInfoTip, TreeView_ShowInfoTip macro [Windows Controls], _shell_TreeView_ShowInfoTip, _shell_TreeView_ShowInfoTip_cpp, commctrl/TreeView_ShowInfoTip, controls.TreeView_ShowInfoTip, controls._shell_TreeView_ShowInfoTip
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
 - TreeView_ShowInfoTip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- TreeView_ShowInfoTip
: 
---

# TreeView_ShowInfoTip macro


## -description


Shows the infotip for a specified item in a tree-view control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb773779(v=VS.85).aspx">TVM_SHOWINFOTIP</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control.


### -param hitem

Type: <b>HITEM</b>

Handle to the item.


## -remarks



Most applications do not use this macro. Infotips are shown automatically. For more information, see Using Tree-view Infotips in the <a href="https://msdn.microsoft.com/en-us/library/Bb760017(v=VS.85).aspx">About Tree-View Controls</a> overview.
        	



