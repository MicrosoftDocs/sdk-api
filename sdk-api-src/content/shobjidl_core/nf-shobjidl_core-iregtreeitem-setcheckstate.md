---
UID: NF:shobjidl_core.IRegTreeItem.SetCheckState
title: IRegTreeItem::SetCheckState (shobjidl_core.h)
description: Sets the state of a check box item in a tree-view control.
helpviewer_keywords: ["FALSE","IRegTreeItem interface [Windows Shell]","SetCheckState method","IRegTreeItem.SetCheckState","IRegTreeItem::SetCheckState","SetCheckState","SetCheckState method [Windows Shell]","SetCheckState method [Windows Shell]","IRegTreeItem interface","TRUE","_win32_IRegTreeItem_SetCheckState","shell.IRegTreeItem_SetCheckState","shobjidl_core/IRegTreeItem::SetCheckState"]
old-location: shell\IRegTreeItem_SetCheckState.htm
tech.root: shell
ms.assetid: 0ba25491-8d18-4040-a256-9078b91e4f3f
ms.date: 12/05/2018
ms.keywords: FALSE, IRegTreeItem interface [Windows Shell],SetCheckState method, IRegTreeItem.SetCheckState, IRegTreeItem::SetCheckState, SetCheckState, SetCheckState method [Windows Shell], SetCheckState method [Windows Shell],IRegTreeItem interface, TRUE, _win32_IRegTreeItem_SetCheckState, shell.IRegTreeItem_SetCheckState, shobjidl_core/IRegTreeItem::SetCheckState
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRegTreeItem::SetCheckState
 - shobjidl_core/IRegTreeItem::SetCheckState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRegTreeItem.SetCheckState
---

# IRegTreeItem::SetCheckState


## -description

Sets the state of a check box item in a tree-view control.

## -parameters

### -param bCheck [in]

Type: <b>BOOL</b>

A <b>BOOL</b> that sets the state of the check box.
        



#### TRUE

The check box is checked.



#### FALSE

The check box is not checked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iregtreeitem">IRegTreeItem</a>



<a href="/windows/desktop/Controls/tree-view-controls">Tree-View Controls</a>