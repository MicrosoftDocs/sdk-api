---
UID: NF:shlwapi.PathCreateFromUrlAlloc
title: PathCreateFromUrlAlloc function (shlwapi.h)
description: Creates a path from a file URL.
helpviewer_keywords: ["PathCreateFromUrlAlloc","PathCreateFromUrlAlloc function [Windows Shell]","_shell_PathCreateFromUrlAlloc","shell.PathCreateFromUrlAlloc","shlwapi/PathCreateFromUrlAlloc"]
old-location: shell\PathCreateFromUrlAlloc.htm
tech.root: shell
ms.assetid: 274411cd-5922-4db8-8775-feb93cae32dd
ms.date: 12/05/2018
ms.keywords: PathCreateFromUrlAlloc, PathCreateFromUrlAlloc function [Windows Shell], _shell_PathCreateFromUrlAlloc, shell.PathCreateFromUrlAlloc, shlwapi/PathCreateFromUrlAlloc
req.header: shlwapi.h
req.include-header: 
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
req.dll: Shlwapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathCreateFromUrlAlloc
 - shlwapi/PathCreateFromUrlAlloc
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
 - PathCreateFromUrlAlloc
---

# PathCreateFromUrlAlloc function


## -description

Creates a path from a file URL.

## -parameters

### -param pszIn [in]

Type: <b>PCWSTR</b>

A pointer to the URL of a file, represented as a null-terminated, Unicode string.

### -param ppszOut [out]

Type: <b>PWSTR*</b>

The address of a pointer to a buffer of length MAX_PATH that, when this function returns successfully, receives the file path.

### -param dwFlags

Type: <b>DWORD</b>

Reserved, must be 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

