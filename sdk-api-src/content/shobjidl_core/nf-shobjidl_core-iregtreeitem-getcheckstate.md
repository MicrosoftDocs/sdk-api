---
UID: NF:shobjidl_core.IRegTreeItem.GetCheckState
title: IRegTreeItem::GetCheckState (shobjidl_core.h)
description: Gets the state of a check box item in a tree-view control.
helpviewer_keywords: ["FALSE","GetCheckState","GetCheckState method [Windows Shell]","GetCheckState method [Windows Shell]","IRegTreeItem interface","IRegTreeItem interface [Windows Shell]","GetCheckState method","IRegTreeItem.GetCheckState","IRegTreeItem::GetCheckState","TRUE","_win32_IRegTreeItem_GetCheckState","shell.IRegTreeItem_GetCheckState","shobjidl_core/IRegTreeItem::GetCheckState"]
old-location: shell\IRegTreeItem_GetCheckState.htm
tech.root: shell
ms.assetid: bfeff83e-8872-4df2-a519-1335be6e443c
ms.date: 12/05/2018
ms.keywords: FALSE, GetCheckState, GetCheckState method [Windows Shell], GetCheckState method [Windows Shell],IRegTreeItem interface, IRegTreeItem interface [Windows Shell],GetCheckState method, IRegTreeItem.GetCheckState, IRegTreeItem::GetCheckState, TRUE, _win32_IRegTreeItem_GetCheckState, shell.IRegTreeItem_GetCheckState, shobjidl_core/IRegTreeItem::GetCheckState
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
 - IRegTreeItem::GetCheckState
 - shobjidl_core/IRegTreeItem::GetCheckState
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
 - IRegTreeItem.GetCheckState
---

# IRegTreeItem::GetCheckState


## -description

Gets the state of a check box item in a tree-view control.

## -parameters

### -param pbCheck [out]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> that contains the state of the check box.



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