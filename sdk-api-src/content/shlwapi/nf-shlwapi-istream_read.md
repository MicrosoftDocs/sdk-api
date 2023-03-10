---
UID: NF:shlwapi.IStream_Read
title: IStream_Read function (shlwapi.h)
description: Reads bytes from a specified stream and returns a value that indicates whether all bytes were successfully read.
helpviewer_keywords: ["IStream_Read","IStream_Read function [Windows Shell]","_win32_IStream_Read","shell.IStream_Read","shlwapi/IStream_Read"]
old-location: shell\IStream_Read.htm
tech.root: shell
ms.assetid: 07a3a500-babb-458b-ba98-9344c63ea014
ms.date: 12/05/2018
ms.keywords: IStream_Read, IStream_Read function [Windows Shell], _win32_IStream_Read, shell.IStream_Read, shlwapi/IStream_Read
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStream_Read
 - shlwapi/IStream_Read
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
 - IStream_Read
---

# IStream_Read function


## -description

Reads bytes from a specified stream and returns a value that indicates whether all bytes were successfully read.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of the stream from which to read.

### -param pv [out]

Type: <b>VOID*</b>

A pointer to a buffer to receive the stream data from <i>pstm</i>. This buffer must be at least <i>cb</i> bytes in size.

### -param cb [in]

Type: <b>ULONG</b>

The number of bytes of data that the function should attempt to read from the input stream.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the function successfully reads the specified number of bytes from the stream, or a COM failure code otherwise. In particular, if the read attempt was successful but fewer than <i>cb</i> bytes were read, the function returns <b>E_FAIL</b>.

## -remarks

This function calls the <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> method to read data from the specified stream into the buffer. If the function fails for any reason, the contents of the output buffer and the position of the read pointer in the input stream are undefined.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a>