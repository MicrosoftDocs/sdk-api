---
UID: NF:shobjidl_core.SHCreateItemWithParent
title: SHCreateItemWithParent function (shobjidl_core.h)
description: Create a Shell item, given a parent folder and a child item ID.
helpviewer_keywords: ["SHCreateItemWithParent","SHCreateItemWithParent function [Windows Shell]","_shell_SHCreateItemWithParent","shell.SHCreateItemWithParent","shobjidl_core/SHCreateItemWithParent"]
old-location: shell\SHCreateItemWithParent.htm
tech.root: shell
ms.assetid: 8fb84a20-d8f2-4c7c-bfb1-a22791b8636a
ms.date: 12/05/2018
ms.keywords: SHCreateItemWithParent, SHCreateItemWithParent function [Windows Shell], _shell_SHCreateItemWithParent, shell.SHCreateItemWithParent, shobjidl_core/SHCreateItemWithParent
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
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateItemWithParent
 - shobjidl_core/SHCreateItemWithParent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - ext-ms-win-shell-shell32-l1-2-2.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHCreateItemWithParent
---

# SHCreateItemWithParent function


## -description

Create a Shell item, given a parent folder and a child item ID.

## -parameters

### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The IDList of the parent folder of the item being created; the IDList of <i>psfParent</i>. This parameter can be <b>NULL</b>, if <i>psfParent</i> is specified.

### -param psfParent [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface that specifies the shell data source of the child item specified by the <i>pidl</i>.This parameter can be <b>NULL</b>, if <i>pidlParent</i> is specified.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A child item ID relative to its parent folder specified by <i>psfParent</i> or <i>pidlParent</i>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to an interface ID.

### -param ppvItem [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid.  This will typically be <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or 
        <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.