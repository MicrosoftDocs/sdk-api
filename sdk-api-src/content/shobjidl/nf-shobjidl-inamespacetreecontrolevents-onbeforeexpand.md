---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnBeforeExpand
title: INameSpaceTreeControlEvents::OnBeforeExpand (shobjidl.h)
description: Called before an IShellItem is expanded.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnBeforeExpand method","INameSpaceTreeControlEvents.OnBeforeExpand","INameSpaceTreeControlEvents::OnBeforeExpand","OnBeforeExpand","OnBeforeExpand method [Windows Shell]","OnBeforeExpand method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnBeforeExpand","shell.INameSpaceTreeControlEvents_OnBeforeExpand","shobjidl/INameSpaceTreeControlEvents::OnBeforeExpand"]
old-location: shell\INameSpaceTreeControlEvents_OnBeforeExpand.htm
tech.root: shell
ms.assetid: b3cf5edf-061a-434a-b273-dc33fcdd8448
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnBeforeExpand method, INameSpaceTreeControlEvents.OnBeforeExpand, INameSpaceTreeControlEvents::OnBeforeExpand, OnBeforeExpand, OnBeforeExpand method [Windows Shell], OnBeforeExpand method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnBeforeExpand, shell.INameSpaceTreeControlEvents_OnBeforeExpand, shobjidl/INameSpaceTreeControlEvents::OnBeforeExpand
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
 - INameSpaceTreeControlEvents::OnBeforeExpand
 - shobjidl/INameSpaceTreeControlEvents::OnBeforeExpand
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
 - INameSpaceTreeControlEvents.OnBeforeExpand
---

# INameSpaceTreeControlEvents::OnBeforeExpand


## -description

Called before an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is expanded.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that is to be expanded.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>