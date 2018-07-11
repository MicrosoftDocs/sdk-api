---
UID: NF:commctrl.TreeView_MapHTREEITEMToAccID
title: TreeView_MapHTREEITEMToAccID macro
author: windows-sdk-content
description: Maps an HTREEITEM to an accessibility ID. You can use this macro or send the TVM_MAPHTREEITEMTOACCID message explicitly.
old-location: controls\TreeView_MapHTREEITEMToAccID.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_maphtreeitemtoaccid.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: TreeView_MapHTREEITEMToAccID, TreeView_MapHTREEITEMtoAccID, TreeView_MapHTREEITEMtoAccID macro [Windows Controls], _win32_TreeView_MapHTREEITEMToAccID, _win32_TreeView_MapHTREEITEMToAccID_cpp, commctrl/TreeView_MapHTREEITEMtoAccID, controls.TreeView_MapHTREEITEMToAccID, controls._win32_TreeView_MapHTREEITEMToAccID
ms.prod: windows
ms.technology: windows-sdk
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
 - TreeView_MapHTREEITEMtoAccID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TreeView_MapHTREEITEMToAccID macro


## -description


Maps an <b>HTREEITEM</b> to an accessibility ID. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb773735(v=VS.85).aspx">TVM_MAPHTREEITEMTOACCID</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the list-view control. 


### -param htreeitem

Type: <b>HTREEITEM</b>

The value to be mapped.


## -remarks



To use <b>TreeView_MapHTREEITEMtoAccID</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 

<div class="alert"><b>Note</b>  The accessibility ID is not the same as that mentioned in <a href="https://msdn.microsoft.com/bac49a2d-4357-4607-a89d-d2ed4abf89bb">IAccessibleObject</a>. This is a unique ID used for treeview items as long as treeitems do not exceed the max limit of <b>UINT</b>.
</div>
<div> </div>


