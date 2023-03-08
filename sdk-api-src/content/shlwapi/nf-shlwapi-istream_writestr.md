---
UID: NF:shlwapi.IStream_WriteStr
title: IStream_WriteStr function (shlwapi.h)
description: Reads from a string and writes into a stream.
helpviewer_keywords: ["IStream_WriteStr","IStream_WriteStr function [Windows Shell]","_shell_IStream_WriteStr","shell.IStream_WriteStr","shlwapi/IStream_WriteStr"]
old-location: shell\IStream_WriteStr.htm
tech.root: shell
ms.assetid: 13292ccd-fc0c-4230-a935-4d5aed8cec97
ms.date: 12/05/2018
ms.keywords: IStream_WriteStr, IStream_WriteStr function [Windows Shell], _shell_IStream_WriteStr, shell.IStream_WriteStr, shlwapi/IStream_WriteStr
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
 - IStream_WriteStr
 - shlwapi/IStream_WriteStr
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
 - IStream_WriteStr
---

# IStream_WriteStr function


## -description

Reads from a string and writes into a stream.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the stream in which to write.

### -param psz [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string from which to read.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.