---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDragEnter
title: INameSpaceTreeControlDropHandler::OnDragEnter (shobjidl.h)
description: Called on drag enter to set drag effect, as specified.
helpviewer_keywords: ["INameSpaceTreeControlDropHandler interface [Windows Shell]","OnDragEnter method","INameSpaceTreeControlDropHandler.OnDragEnter","INameSpaceTreeControlDropHandler::OnDragEnter","OnDragEnter","OnDragEnter method [Windows Shell]","OnDragEnter method [Windows Shell]","INameSpaceTreeControlDropHandler interface","_shell_INameSpaceTreeControlDropHandler_OnDragEnter","shell.INameSpaceTreeControlDropHandler_OnDragEnter","shobjidl/INameSpaceTreeControlDropHandler::OnDragEnter"]
old-location: shell\INameSpaceTreeControlDropHandler_OnDragEnter.htm
tech.root: shell
ms.assetid: b9a87024-d62e-4006-a716-c1461d9c9ffe
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDragEnter method, INameSpaceTreeControlDropHandler.OnDragEnter, INameSpaceTreeControlDropHandler::OnDragEnter, OnDragEnter, OnDragEnter method [Windows Shell], OnDragEnter method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDragEnter, shell.INameSpaceTreeControlDropHandler_OnDragEnter, shobjidl/INameSpaceTreeControlDropHandler::OnDragEnter
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INameSpaceTreeControlDropHandler::OnDragEnter
 - shobjidl/INameSpaceTreeControlDropHandler::OnDragEnter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlDropHandler.OnDragEnter
---

# INameSpaceTreeControlDropHandler::OnDragEnter


## -description

Called on drag enter to set drag effect, as specified.

## -parameters

### -param psiOver [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.

### -param psiaData [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array containing the items being dragged.

### -param fOutsideSource [in]

Type: <b>BOOL</b>

Specifies whether drag started outside target area.

### -param grfKeyState [in]

Type: <b>DWORD</b>

The current state of keyboard modifier keys.

### -param pdwEffect [in, out]

Type: <b>DWORD*</b>

On success, contains a pointer to the drag effect value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Failing this method blocks the drag operation in the namespace tree control (NSTC).

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a>



<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontroldrophandler">INameSpaceTreeControlDropHandler</a>