---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnBeforeItemDelete
title: INameSpaceTreeControlEvents::OnBeforeItemDelete (shobjidl.h)
description: Called before an IShellItem and all of its children are deleted.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnBeforeItemDelete method","INameSpaceTreeControlEvents.OnBeforeItemDelete","INameSpaceTreeControlEvents::OnBeforeItemDelete","OnBeforeItemDelete","OnBeforeItemDelete method [Windows Shell]","OnBeforeItemDelete method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnBeforeItemDelete","shell.INameSpaceTreeControlEvents_OnBeforeItemDelete","shobjidl/INameSpaceTreeControlEvents::OnBeforeItemDelete"]
old-location: shell\INameSpaceTreeControlEvents_OnBeforeItemDelete.htm
tech.root: shell
ms.assetid: 6d602c9d-7305-41d3-b757-3e9e125c6cbd
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnBeforeItemDelete method, INameSpaceTreeControlEvents.OnBeforeItemDelete, INameSpaceTreeControlEvents::OnBeforeItemDelete, OnBeforeItemDelete, OnBeforeItemDelete method [Windows Shell], OnBeforeItemDelete method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnBeforeItemDelete, shell.INameSpaceTreeControlEvents_OnBeforeItemDelete, shobjidl/INameSpaceTreeControlEvents::OnBeforeItemDelete
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
 - INameSpaceTreeControlEvents::OnBeforeItemDelete
 - shobjidl/INameSpaceTreeControlEvents::OnBeforeItemDelete
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
 - INameSpaceTreeControlEvents.OnBeforeItemDelete
---

# INameSpaceTreeControlEvents::OnBeforeItemDelete


## -description

Called before an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> and all of its children are deleted.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that is to be deleted.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method fails, the given <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> and its children are still deleted.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>