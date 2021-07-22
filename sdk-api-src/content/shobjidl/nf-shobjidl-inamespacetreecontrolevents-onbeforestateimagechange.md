---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnBeforeStateImageChange
title: INameSpaceTreeControlEvents::OnBeforeStateImageChange (shobjidl.h)
description: Called before the state icon of the given IShellItem is changed.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnBeforeStateImageChange method","INameSpaceTreeControlEvents.OnBeforeStateImageChange","INameSpaceTreeControlEvents::OnBeforeStateImageChange","OnBeforeStateImageChange","OnBeforeStateImageChange method [Windows Shell]","OnBeforeStateImageChange method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnBeforeStateImageChange","shell.INameSpaceTreeControlEvents_OnBeforeStateImageChange","shobjidl/INameSpaceTreeControlEvents::OnBeforeStateImageChange"]
old-location: shell\INameSpaceTreeControlEvents_OnBeforeStateImageChange.htm
tech.root: shell
ms.assetid: c26296ae-f11c-4fe9-a74c-c97472dbcb1e
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnBeforeStateImageChange method, INameSpaceTreeControlEvents.OnBeforeStateImageChange, INameSpaceTreeControlEvents::OnBeforeStateImageChange, OnBeforeStateImageChange, OnBeforeStateImageChange method [Windows Shell], OnBeforeStateImageChange method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnBeforeStateImageChange, shell.INameSpaceTreeControlEvents_OnBeforeStateImageChange, shobjidl/INameSpaceTreeControlEvents::OnBeforeStateImageChange
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
 - INameSpaceTreeControlEvents::OnBeforeStateImageChange
 - shobjidl/INameSpaceTreeControlEvents::OnBeforeStateImageChange
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
 - INameSpaceTreeControlEvents.OnBeforeStateImageChange
---

# INameSpaceTreeControlEvents::OnBeforeStateImageChange


## -description

Called before the state icon of the given <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is changed.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> in which the state image is changing.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method returns S_OK, the client has processed the event and no further action is required of the namespace control. Otherwise the event will need to be processed, in this case the default action is to go to the next image in the list.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>