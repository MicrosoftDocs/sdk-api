---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDrop
title: INameSpaceTreeControlDropHandler::OnDrop (shobjidl.h)
description: Called on drop to set drop effect, as specified.
helpviewer_keywords: ["INameSpaceTreeControlDropHandler interface [Windows Shell]","OnDrop method","INameSpaceTreeControlDropHandler.OnDrop","INameSpaceTreeControlDropHandler::OnDrop","OnDrop","OnDrop method [Windows Shell]","OnDrop method [Windows Shell]","INameSpaceTreeControlDropHandler interface","_shell_INameSpaceTreeControlDropHandler_OnDrop","shell.INameSpaceTreeControlDropHandler_OnDrop","shobjidl/INameSpaceTreeControlDropHandler::OnDrop"]
old-location: shell\INameSpaceTreeControlDropHandler_OnDrop.htm
tech.root: shell
ms.assetid: 05c677fb-a2e2-4aa5-bb27-4dc437ca408c
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDrop method, INameSpaceTreeControlDropHandler.OnDrop, INameSpaceTreeControlDropHandler::OnDrop, OnDrop, OnDrop method [Windows Shell], OnDrop method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDrop, shell.INameSpaceTreeControlDropHandler_OnDrop, shobjidl/INameSpaceTreeControlDropHandler::OnDrop
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
 - INameSpaceTreeControlDropHandler::OnDrop
 - shobjidl/INameSpaceTreeControlDropHandler::OnDrop
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
 - INameSpaceTreeControlDropHandler.OnDrop
---

# INameSpaceTreeControlDropHandler::OnDrop


## -description

Called on drop to set drop effect, as specified.

## -parameters

### -param psiOver [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.

### -param psiaData [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array representing a data object.

### -param iPosition [in]

Type: <b>int</b>

Specifies drop position.

### -param grfKeyState [in]

Type: <b>DWORD</b>

The current state of keyboard modifier keys.

### -param pdwEffect [in, out]

Type: <b>DWORD*</b>

A pointer to the drop effect value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  To overwrite the default drop behavior, a client should fail this method; success proceeds with the default drop operation.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a>



<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontroldrophandler">INameSpaceTreeControlDropHandler</a>