---
UID: NF:shlwapi.IStream_Copy
title: IStream_Copy function (shlwapi.h)
description: Copies a stream to another stream.
helpviewer_keywords: ["IStream_Copy","IStream_Copy function [Windows Shell]","_shell_IStream_Copy","shell.IStream_Copy","shlwapi/IStream_Copy"]
old-location: shell\IStream_Copy.htm
tech.root: shell
ms.assetid: 7d6a1080-dad4-4821-8f2a-bd1e01ca10cf
ms.date: 12/05/2018
ms.keywords: IStream_Copy, IStream_Copy function [Windows Shell], _shell_IStream_Copy, shell.IStream_Copy, shlwapi/IStream_Copy
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
 - IStream_Copy
 - shlwapi/IStream_Copy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-stream-l1-1-0.dll
api_name:
 - IStream_Copy
---

# IStream_Copy function


## -description

Copies a stream to another stream.

## -parameters

### -param pstmFrom [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the source stream.

### -param pstmTo [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the destination stream.

### -param cb [in]

Type: <b>DWORD</b>

The number of bytes to copy from the source stream.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.