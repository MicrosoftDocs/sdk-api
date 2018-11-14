---
UID: NF:commctrl.TreeView_MapAccIDToHTREEITEM
title: TreeView_MapAccIDToHTREEITEM macro
author: windows-sdk-content
description: Maps an accessibility ID to an HTREEITEM. You can use this macro or send the TVM_MAPACCIDTOHTREEITEM message explicitly.
old-location: controls\TreeView_MapAccIDToHTREEITEM.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_mapaccidtohtreeitem.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TreeView_MapAccIDToHTREEITEM, TreeView_MapAccIDToHTREEITEM macro [Windows Controls], _win32_TreeView_MapAccIDToHTREEITEM, _win32_TreeView_MapAccIDToHTREEITEM_cpp, commctrl/TreeView_MapAccIDToHTREEITEM, controls.TreeView_MapAccIDToHTREEITEM, controls._win32_TreeView_MapAccIDToHTREEITEM
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
 - TreeView_MapAccIDToHTREEITEM
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
- TreeView_MapAccIDToHTREEITEM
: 
---

# TreeView_MapAccIDToHTREEITEM macro


## -description


Maps an accessibility ID to an <b>HTREEITEM</b>. You can use this macro or send the <a href="https://msdn.microsoft.com/f4feb7cb-2138-4930-b8ee-b9e2d4b19001">TVM_MAPACCIDTOHTREEITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param id

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The accessibility ID to map to an <b>HTREEITEM</b>.


## -remarks



To use <b>TreeView_MapAccIDToHTREEITEM</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 

<div class="alert"><b>Note</b>  The accessibility ID is not the same as that mentioned in <a href="https://msdn.microsoft.com/bac49a2d-4357-4607-a89d-d2ed4abf89bb">IAccessibleObject</a>. This is a unique ID used for treeview items as long as treeitems do not exceed the max limit of <b>UINT</b>.
</div>
<div> </div>


