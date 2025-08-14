---
UID: NF:shobjidl_core.SHGetIDListFromObject
title: SHGetIDListFromObject function (shobjidl_core.h)
description: Retrieves the pointer to an item identifier list (PIDL) of an object.
helpviewer_keywords: ["SHGetIDListFromObject","SHGetIDListFromObject function [Windows Shell]","_shell_SHGetIDListFromObject","shell.SHGetIDListFromObject","shobjidl_core/SHGetIDListFromObject"]
old-location: shell\SHGetIDListFromObject.htm
tech.root: shell
ms.assetid: 42821075-8123-4bfa-a6ba-8d3a77a9f50b
ms.date: 12/05/2018
ms.keywords: SHGetIDListFromObject, SHGetIDListFromObject function [Windows Shell], _shell_SHGetIDListFromObject, shell.SHGetIDListFromObject, shobjidl_core/SHGetIDListFromObject
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
 - SHGetIDListFromObject
 - shobjidl_core/SHGetIDListFromObject
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
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHGetIDListFromObject
---

# SHGetIDListFromObject function


## -description

Retrieves the pointer to an item identifier list (PIDL) of an object.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the object from which to get the PIDL.

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this function returns, contains a pointer to the PIDL of the given object.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist">SHCreateItemFromIDList</a>