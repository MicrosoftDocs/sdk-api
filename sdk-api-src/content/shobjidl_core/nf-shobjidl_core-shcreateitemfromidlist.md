---
UID: NF:shobjidl_core.SHCreateItemFromIDList
title: SHCreateItemFromIDList function (shobjidl_core.h)
description: Creates and initializes a Shell item object from a pointer to an item identifier list (PIDL). The resulting shell item object supports the IShellItem interface.
helpviewer_keywords: ["SHCreateItemFromIDList","SHCreateItemFromIDList function [Windows Shell]","_shell_SHCreateItemFromIDList","shell.SHCreateItemFromIDList","shobjidl_core/SHCreateItemFromIDList"]
old-location: shell\SHCreateItemFromIDList.htm
tech.root: shell
ms.assetid: a6dcddd9-cdbc-4cf9-97e3-d1b562283344
ms.date: 12/05/2018
ms.keywords: SHCreateItemFromIDList, SHCreateItemFromIDList function [Windows Shell], _shell_SHCreateItemFromIDList, shell.SHCreateItemFromIDList, shobjidl_core/SHCreateItemFromIDList
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
 - SHCreateItemFromIDList
 - shobjidl_core/SHCreateItemFromIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHCreateItemFromIDList
---

# SHCreateItemFromIDList function


## -description

Creates and initializes a Shell item object from a pointer to an item identifier list (PIDL). The resulting shell item object supports the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The source PIDL.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid.  This will typically be <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or 
        <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject">SHGetIDListFromObject</a>