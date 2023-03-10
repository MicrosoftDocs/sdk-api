---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction
title: INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction (shobjidl.h)
description: Invokes the default accessibility action on a Shell item.
helpviewer_keywords: ["INameSpaceTreeAccessible interface [Windows Shell]","OnDoDefaultAccessibilityAction method","INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction","INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction","OnDoDefaultAccessibilityAction","OnDoDefaultAccessibilityAction method [Windows Shell]","OnDoDefaultAccessibilityAction method [Windows Shell]","INameSpaceTreeAccessible interface","_shell_INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction","shell.INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction","shobjidl/INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction"]
old-location: shell\INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction.htm
tech.root: shell
ms.assetid: a6aa6588-6e3c-4229-8540-0aa5d85c0381
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnDoDefaultAccessibilityAction method, INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction, INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction, OnDoDefaultAccessibilityAction, OnDoDefaultAccessibilityAction method [Windows Shell], OnDoDefaultAccessibilityAction method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction, shell.INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction, shobjidl/INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction
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
 - INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction
 - shobjidl/INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction
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
 - INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction
---

# INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction


## -description

Invokes the default accessibility action on a Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.