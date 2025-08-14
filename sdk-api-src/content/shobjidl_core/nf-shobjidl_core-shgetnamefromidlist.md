---
UID: NF:shobjidl_core.SHGetNameFromIDList
title: SHGetNameFromIDList function (shobjidl_core.h)
description: Retrieves the display name of an item identified by its IDList.
helpviewer_keywords: ["SHGetNameFromIDList","SHGetNameFromIDList function [Windows Shell]","_shell_SHGetNameFromIDList","shell.SHGetNameFromIDList","shobjidl_core/SHGetNameFromIDList"]
old-location: shell\SHGetNameFromIDList.htm
tech.root: shell
ms.assetid: d2fc1eeb-bd76-4bd7-9a4f-4142e53f0afb
ms.date: 12/05/2018
ms.keywords: SHGetNameFromIDList, SHGetNameFromIDList function [Windows Shell], _shell_SHGetNameFromIDList, shell.SHGetNameFromIDList, shobjidl_core/SHGetNameFromIDList
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
 - SHGetNameFromIDList
 - shobjidl_core/SHGetNameFromIDList
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
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHGetNameFromIDList
---

# SHGetNameFromIDList function


## -description

Retrieves the display name of an item identified by its IDList.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that identifies the item.

### -param sigdnName [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn">SIGDN</a></b>

A value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn">SIGDN</a> enumeration that specifies the type of display name to retrieve.

### -param ppszName [out]

Type: <b>PWSTR*</b>

A value that, when this function returns successfully, receives the address of a pointer to the retrieved display name.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is the responsibility of the caller to free the string pointed to by <i>ppszName</i> when it is no longer needed. Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> on *<i>ppszName</i> to free the memory.