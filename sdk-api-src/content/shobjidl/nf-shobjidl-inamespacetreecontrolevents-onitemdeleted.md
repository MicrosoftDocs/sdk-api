---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemDeleted
title: INameSpaceTreeControlEvents::OnItemDeleted (shobjidl.h)
description: Called after an IShellItem has been deleted.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnItemDeleted method","INameSpaceTreeControlEvents.OnItemDeleted","INameSpaceTreeControlEvents::OnItemDeleted","OnItemDeleted","OnItemDeleted method [Windows Shell]","OnItemDeleted method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnItemDeleted","shell.INameSpaceTreeControlEvents_OnItemDeleted","shobjidl/INameSpaceTreeControlEvents::OnItemDeleted"]
old-location: shell\INameSpaceTreeControlEvents_OnItemDeleted.htm
tech.root: shell
ms.assetid: be5894ce-bf4c-4738-9096-da9c9d8688ee
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemDeleted method, INameSpaceTreeControlEvents.OnItemDeleted, INameSpaceTreeControlEvents::OnItemDeleted, OnItemDeleted, OnItemDeleted method [Windows Shell], OnItemDeleted method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemDeleted, shell.INameSpaceTreeControlEvents_OnItemDeleted, shobjidl/INameSpaceTreeControlEvents::OnItemDeleted
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
 - INameSpaceTreeControlEvents::OnItemDeleted
 - shobjidl/INameSpaceTreeControlEvents::OnItemDeleted
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
 - INameSpaceTreeControlEvents.OnItemDeleted
---

# INameSpaceTreeControlEvents::OnItemDeleted


## -description

Called after an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> has been deleted.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that was deleted.

### -param fIsRoot [in]

Type: <b>BOOL</b>

Specifies whether the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that was deleted is a root.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>