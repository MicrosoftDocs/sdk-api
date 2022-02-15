---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction
title: INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction (shobjidl.h)
description: Gets the default accessibility action for a Shell item.
helpviewer_keywords: ["INameSpaceTreeAccessible interface [Windows Shell]","OnGetDefaultAccessibilityAction method","INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction","INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction","OnGetDefaultAccessibilityAction","OnGetDefaultAccessibilityAction method [Windows Shell]","OnGetDefaultAccessibilityAction method [Windows Shell]","INameSpaceTreeAccessible interface","_shell_INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction","shell.INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction","shobjidl/INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction"]
old-location: shell\INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction.htm
tech.root: shell
ms.assetid: 96eaac9c-7fab-4326-a737-4819794a34c6
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnGetDefaultAccessibilityAction method, INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction, INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction, OnGetDefaultAccessibilityAction, OnGetDefaultAccessibilityAction method [Windows Shell], OnGetDefaultAccessibilityAction method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction, shell.INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction, shobjidl/INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
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
 - INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
 - shobjidl/INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
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
 - INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction
---

# INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction


## -description

Gets the default accessibility action for a Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param pbstrDefaultAction [out]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>*</b>

When this method returns, contains a <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> that specifies the default, accessibility action.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or E_OUTOFMEMORY otherwise.

## -remarks

This method is called when the default accessibility action for a Shell item is retrieved.