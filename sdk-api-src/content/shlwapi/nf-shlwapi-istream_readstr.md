---
UID: NF:shlwapi.IStream_ReadStr
title: IStream_ReadStr function (shlwapi.h)
description: Reads from a stream and writes into a string.
helpviewer_keywords: ["IStream_ReadStr","IStream_ReadStr function [Windows Shell]","_shell_IStream_ReadStr","shell.IStream_ReadStr","shlwapi/IStream_ReadStr"]
old-location: shell\IStream_ReadStr.htm
tech.root: shell
ms.assetid: e3f140c4-4033-4c82-af2c-4a7744461920
ms.date: 12/05/2018
ms.keywords: IStream_ReadStr, IStream_ReadStr function [Windows Shell], _shell_IStream_ReadStr, shell.IStream_ReadStr, shlwapi/IStream_ReadStr
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
 - IStream_ReadStr
 - shlwapi/IStream_ReadStr
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
 - IStream_ReadStr
---

# IStream_ReadStr function


## -description

Reads from a stream and writes into a string.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the stream from which to read.

### -param ppsz [out]

Type: <b>PWSTR*</b>

A pointer to the null-terminated, Unicode string into which the stream is written.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.