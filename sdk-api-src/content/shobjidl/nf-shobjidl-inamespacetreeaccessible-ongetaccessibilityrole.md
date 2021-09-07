---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnGetAccessibilityRole
title: INameSpaceTreeAccessible::OnGetAccessibilityRole (shobjidl.h)
description: Gets the accessibility role for a Shell item.
helpviewer_keywords: ["INameSpaceTreeAccessible interface [Windows Shell]","OnGetAccessibilityRole method","INameSpaceTreeAccessible.OnGetAccessibilityRole","INameSpaceTreeAccessible::OnGetAccessibilityRole","OnGetAccessibilityRole","OnGetAccessibilityRole method [Windows Shell]","OnGetAccessibilityRole method [Windows Shell]","INameSpaceTreeAccessible interface","_shell_INameSpaceTreeAccessible_OnGetAccessibilityRole","shell.INameSpaceTreeAccessible_OnGetAccessibilityRole","shobjidl/INameSpaceTreeAccessible::OnGetAccessibilityRole"]
old-location: shell\INameSpaceTreeAccessible_OnGetAccessibilityRole.htm
tech.root: shell
ms.assetid: 9de27a09-dc11-46a6-a233-696ccf35aa87
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnGetAccessibilityRole method, INameSpaceTreeAccessible.OnGetAccessibilityRole, INameSpaceTreeAccessible::OnGetAccessibilityRole, OnGetAccessibilityRole, OnGetAccessibilityRole method [Windows Shell], OnGetAccessibilityRole method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnGetAccessibilityRole, shell.INameSpaceTreeAccessible_OnGetAccessibilityRole, shobjidl/INameSpaceTreeAccessible::OnGetAccessibilityRole
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
 - INameSpaceTreeAccessible::OnGetAccessibilityRole
 - shobjidl/INameSpaceTreeAccessible::OnGetAccessibilityRole
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
 - INameSpaceTreeAccessible.OnGetAccessibilityRole
---

# INameSpaceTreeAccessible::OnGetAccessibilityRole


## -description

Gets the accessibility role for a Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param pvarRole [out]

Type: <b>VARIANT*</b>

When this method returns, contains a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that specifies the role.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called when the accessibility role for a Shell item is retrieved.