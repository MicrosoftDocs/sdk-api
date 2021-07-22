---
UID: NF:shobjidl_core.INameSpaceTreeControl.EnsureItemVisible
title: INameSpaceTreeControl::EnsureItemVisible (shobjidl_core.h)
description: Ensures that the given item is visible.
helpviewer_keywords: ["EnsureItemVisible","EnsureItemVisible method [Windows Shell]","EnsureItemVisible method [Windows Shell]","INameSpaceTreeControl interface","INameSpaceTreeControl interface [Windows Shell]","EnsureItemVisible method","INameSpaceTreeControl.EnsureItemVisible","INameSpaceTreeControl::EnsureItemVisible","_shell_INameSpaceTreeControl_EnsureItemVisible","shell.INameSpaceTreeControl_EnsureItemVisible","shobjidl_core/INameSpaceTreeControl::EnsureItemVisible"]
old-location: shell\INameSpaceTreeControl_EnsureItemVisible.htm
tech.root: shell
ms.assetid: c0c40137-e19b-448c-a327-454b12a5604a
ms.date: 12/05/2018
ms.keywords: EnsureItemVisible, EnsureItemVisible method [Windows Shell], EnsureItemVisible method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],EnsureItemVisible method, INameSpaceTreeControl.EnsureItemVisible, INameSpaceTreeControl::EnsureItemVisible, _shell_INameSpaceTreeControl_EnsureItemVisible, shell.INameSpaceTreeControl_EnsureItemVisible, shobjidl_core/INameSpaceTreeControl::EnsureItemVisible
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - INameSpaceTreeControl::EnsureItemVisible
 - shobjidl_core/INameSpaceTreeControl::EnsureItemVisible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.EnsureItemVisible
---

# INameSpaceTreeControl::EnsureItemVisible


## -description

Ensures that the given item is visible.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item for which the visibility is being ensured.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.