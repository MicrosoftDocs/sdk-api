---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDragLeave
title: INameSpaceTreeControlDropHandler::OnDragLeave (shobjidl.h)
description: Called on drag leave for a specified item.
helpviewer_keywords: ["INameSpaceTreeControlDropHandler interface [Windows Shell]","OnDragLeave method","INameSpaceTreeControlDropHandler.OnDragLeave","INameSpaceTreeControlDropHandler::OnDragLeave","OnDragLeave","OnDragLeave method [Windows Shell]","OnDragLeave method [Windows Shell]","INameSpaceTreeControlDropHandler interface","_shell_INameSpaceTreeControlDropHandler_OnDragLeave","shell.INameSpaceTreeControlDropHandler_OnDragLeave","shobjidl/INameSpaceTreeControlDropHandler::OnDragLeave"]
old-location: shell\INameSpaceTreeControlDropHandler_OnDragLeave.htm
tech.root: shell
ms.assetid: b5c67541-dcc2-412f-84aa-df0b0d135597
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDragLeave method, INameSpaceTreeControlDropHandler.OnDragLeave, INameSpaceTreeControlDropHandler::OnDragLeave, OnDragLeave, OnDragLeave method [Windows Shell], OnDragLeave method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDragLeave, shell.INameSpaceTreeControlDropHandler_OnDragLeave, shobjidl/INameSpaceTreeControlDropHandler::OnDragLeave
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
 - INameSpaceTreeControlDropHandler::OnDragLeave
 - shobjidl/INameSpaceTreeControlDropHandler::OnDragLeave
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
 - INameSpaceTreeControlDropHandler.OnDragLeave
---

# INameSpaceTreeControlDropHandler::OnDragLeave


## -description

Called on drag leave for a specified item.

## -parameters

### -param psiOver [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a>



<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontroldrophandler">INameSpaceTreeControlDropHandler</a>