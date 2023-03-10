---
UID: NF:shlwapi.HashData
title: HashData function (shlwapi.h)
description: Hashes an array of data.
helpviewer_keywords: ["HashData","HashData function [Windows Shell]","_win32_HashData","shell.HashData","shlwapi/HashData"]
old-location: shell\HashData.htm
tech.root: shell
ms.assetid: 7b42b3ae-c021-49be-b5a7-d3bc0a5d346a
ms.date: 12/05/2018
ms.keywords: HashData, HashData function [Windows Shell], _win32_HashData, shell.HashData, shlwapi/HashData
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HashData
 - shlwapi/HashData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - HashData
---

# HashData function


## -description

Hashes an array of data.

## -parameters

### -param pbData [in]

Type: <b>BYTE*</b>

A pointer to the data array.

### -param cbData

Type: <b>DWORD</b>

The number of elements in the array at <i>pbData</i>.

### -param pbHash [out]

Type: <b>BYTE*</b>

A pointer to a value that, when this function returns successfully, receives the hashed array.

### -param cbHash

Type: <b>DWORD</b>

The number of elements in <i>pbHash</i>. It should be no larger than 256.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

