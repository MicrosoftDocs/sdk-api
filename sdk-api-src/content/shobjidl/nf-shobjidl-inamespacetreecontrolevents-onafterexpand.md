---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnAfterExpand
title: INameSpaceTreeControlEvents::OnAfterExpand (shobjidl.h)
description: Called after an IShellItem is expanded.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnAfterExpand method","INameSpaceTreeControlEvents.OnAfterExpand","INameSpaceTreeControlEvents::OnAfterExpand","OnAfterExpand","OnAfterExpand method [Windows Shell]","OnAfterExpand method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnAfterExpand","shell.INameSpaceTreeControlEvents_OnAfterExpand","shobjidl/INameSpaceTreeControlEvents::OnAfterExpand"]
old-location: shell\INameSpaceTreeControlEvents_OnAfterExpand.htm
tech.root: shell
ms.assetid: cdc43044-9d0a-4def-956a-f1031314d4cb
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnAfterExpand method, INameSpaceTreeControlEvents.OnAfterExpand, INameSpaceTreeControlEvents::OnAfterExpand, OnAfterExpand, OnAfterExpand method [Windows Shell], OnAfterExpand method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnAfterExpand, shell.INameSpaceTreeControlEvents_OnAfterExpand, shobjidl/INameSpaceTreeControlEvents::OnAfterExpand
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
 - INameSpaceTreeControlEvents::OnAfterExpand
 - shobjidl/INameSpaceTreeControlEvents::OnAfterExpand
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
 - INameSpaceTreeControlEvents.OnAfterExpand
---

# INameSpaceTreeControlEvents::OnAfterExpand


## -description

Called after an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is expanded.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that was expanded.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>