---
UID: NF:commctrl.TreeView_MapHTREEITEMToAccID
title: TreeView_MapHTREEITEMToAccID macro (commctrl.h)
description: Maps an HTREEITEM to an accessibility ID. You can use this macro or send the TVM_MAPHTREEITEMTOACCID message explicitly.helpviewer_keywords: ["TreeView_MapHTREEITEMToAccID","TreeView_MapHTREEITEMtoAccID","TreeView_MapHTREEITEMtoAccID macro [Windows Controls]","_win32_TreeView_MapHTREEITEMToAccID","_win32_TreeView_MapHTREEITEMToAccID_cpp","commctrl/TreeView_MapHTREEITEMtoAccID","controls.TreeView_MapHTREEITEMToAccID","controls._win32_TreeView_MapHTREEITEMToAccID"]
old-location: controls\TreeView_MapHTREEITEMToAccID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_maphtreeitemtoaccid.htm
ms.date: 12/05/2018
ms.keywords: TreeView_MapHTREEITEMToAccID, TreeView_MapHTREEITEMtoAccID, TreeView_MapHTREEITEMtoAccID macro [Windows Controls], _win32_TreeView_MapHTREEITEMToAccID, _win32_TreeView_MapHTREEITEMToAccID_cpp, commctrl/TreeView_MapHTREEITEMtoAccID, controls.TreeView_MapHTREEITEMToAccID, controls._win32_TreeView_MapHTREEITEMToAccID
f1_keywords:
- commctrl/TreeView_MapHTREEITEMtoAccID
dev_langs:
- c++
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
- TreeView_MapHTREEITEMtoAccID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TreeView_MapHTREEITEMToAccID macro


## -description


Maps an <b>HTREEITEM</b> to an accessibility ID. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-maphtreeitemtoaccid">TVM_MAPHTREEITEMTOACCID</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the list-view control. 


### -param htreeitem

Type: <b>HTREEITEM</b>

The value to be mapped.


## -remarks



To use <b>TreeView_MapHTREEITEMtoAccID</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 

<div class="alert"><b>Note</b>  The accessibility ID is not the same as that mentioned in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibleobject">IAccessibleObject</a>. This is a unique ID used for treeview items as long as treeitems do not exceed the max limit of <b>UINT</b>.
</div>
<div> </div>


