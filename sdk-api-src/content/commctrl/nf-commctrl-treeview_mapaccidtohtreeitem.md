---
UID: NF:commctrl.TreeView_MapAccIDToHTREEITEM
title: TreeView_MapAccIDToHTREEITEM macro (commctrl.h)
description: Maps an accessibility ID to an HTREEITEM. You can use this macro or send the TVM_MAPACCIDTOHTREEITEM message explicitly.
helpviewer_keywords: ["TreeView_MapAccIDToHTREEITEM","TreeView_MapAccIDToHTREEITEM macro [Windows Controls]","_win32_TreeView_MapAccIDToHTREEITEM","_win32_TreeView_MapAccIDToHTREEITEM_cpp","commctrl/TreeView_MapAccIDToHTREEITEM","controls.TreeView_MapAccIDToHTREEITEM","controls._win32_TreeView_MapAccIDToHTREEITEM"]
old-location: controls\TreeView_MapAccIDToHTREEITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_mapaccidtohtreeitem.htm
ms.date: 10/21/2024
ms.keywords: TreeView_MapAccIDToHTREEITEM, TreeView_MapAccIDToHTREEITEM macro [Windows Controls], _win32_TreeView_MapAccIDToHTREEITEM, _win32_TreeView_MapAccIDToHTREEITEM_cpp, commctrl/TreeView_MapAccIDToHTREEITEM, controls.TreeView_MapAccIDToHTREEITEM, controls._win32_TreeView_MapAccIDToHTREEITEM
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
 - TreeView_MapAccIDToHTREEITEM
 - commctrl/TreeView_MapAccIDToHTREEITEM
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
 - TreeView_MapAccIDToHTREEITEM
---

# TreeView_MapAccIDToHTREEITEM macro

## -syntax

```cpp
HTREEITEM TreeView_MapAccIDToHTREEITEM(
   HWND hwnd,
   UINT id
);
```

## -returns

Type: **HTREEITEM**

Returns the <b>HTREEITEM</b> to which the specified accessibility ID is mapped.


## -description

Maps an accessibility ID to an <b>HTREEITEM</b>. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-mapaccidtohtreeitem">TVM_MAPACCIDTOHTREEITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param id

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The accessibility ID to map to an <b>HTREEITEM</b>.

## -remarks

To use <b>TreeView_MapAccIDToHTREEITEM</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 

<div class="alert"><b>Note</b>  The accessibility ID is not the same as that mentioned in <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibleobject">IAccessibleObject</a>. This is a unique ID used for treeview items as long as treeitems do not exceed the max limit of <b>UINT</b>.
</div>
<div> </div>
