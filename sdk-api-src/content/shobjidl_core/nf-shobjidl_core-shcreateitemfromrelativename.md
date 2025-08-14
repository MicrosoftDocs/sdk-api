---
UID: NF:shobjidl_core.SHCreateItemFromRelativeName
title: SHCreateItemFromRelativeName function (shobjidl_core.h)
description: Creates and initializes a Shell item object from a relative parsing name.
helpviewer_keywords: ["SHCreateItemFromRelativeName","SHCreateItemFromRelativeName function [Windows Shell]","_shell_SHCreateItemFromRelativeName","shell.SHCreateItemFromRelativeName","shobjidl_core/SHCreateItemFromRelativeName"]
old-location: shell\SHCreateItemFromRelativeName.htm
tech.root: shell
ms.assetid: af6c2e8b-c812-4858-a9db-24549dedc2aa
ms.date: 12/05/2018
ms.keywords: SHCreateItemFromRelativeName, SHCreateItemFromRelativeName function [Windows Shell], _shell_SHCreateItemFromRelativeName, shell.SHCreateItemFromRelativeName, shobjidl_core/SHCreateItemFromRelativeName
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateItemFromRelativeName
 - shobjidl_core/SHCreateItemFromRelativeName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
api_name:
 - SHCreateItemFromRelativeName
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHCreateItemFromRelativeName function


## -description

Creates and initializes a Shell item object from a relative parsing name.

## -parameters

### -param psiParent [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the parent Shell item.

### -param pszName [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string that specifies a display name that is relative to the <i>psiParent</i>.

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to a bind context that controls the parsing operation. This parameter can be <b>NULL</b>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to an interface ID.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid.  This will usually be <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or 
        <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
