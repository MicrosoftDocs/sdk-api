---
UID: NF:shlwapi.IQueryAssociations.GetKey
title: IQueryAssociations::GetKey (shlwapi.h)
description: Searches for and retrieves a file or protocol association-related key from the registry.
helpviewer_keywords: ["GetKey","GetKey method [Windows Shell]","GetKey method [Windows Shell]","IQueryAssociations interface","IQueryAssociations interface [Windows Shell]","GetKey method","IQueryAssociations.GetKey","IQueryAssociations::GetKey","_win32_IQueryAssociations_GetKey","shell.IQueryAssociations_GetKey","shlwapi/IQueryAssociations::GetKey"]
old-location: shell\IQueryAssociations_GetKey.htm
tech.root: shell
ms.assetid: 7f380a9e-fda0-46be-88a1-fd73b0a4b7b7
ms.date: 12/05/2018
ms.keywords: GetKey, GetKey method [Windows Shell], GetKey method [Windows Shell],IQueryAssociations interface, IQueryAssociations interface [Windows Shell],GetKey method, IQueryAssociations.GetKey, IQueryAssociations::GetKey, _win32_IQueryAssociations_GetKey, shell.IQueryAssociations_GetKey, shlwapi/IQueryAssociations::GetKey
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryAssociations::GetKey
 - shlwapi/IQueryAssociations::GetKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryAssociations.GetKey
---

# IQueryAssociations::GetKey


## -description

Searches for and retrieves a file or protocol association-related key from the registry.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/win32/shell/assocf_str">ASSOCF</a></b>

The <a href="/windows/win32/shell/assocf_str">ASSOCF</a> value that can be used to control the search.

### -param key [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-assockey">ASSOCKEY</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-assockey">ASSOCKEY</a> value that specifies the type of key that is to be returned.

### -param pszExtra [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional null-terminated Unicode string with information about the location of the key. It is normally set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.

### -param phkeyOut [out]

Type: <b>HKEY*</b>

A pointer to the key's HKEY value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>