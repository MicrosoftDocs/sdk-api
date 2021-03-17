---
UID: NF:shlwapi.IStream_Size
title: IStream_Size function (shlwapi.h)
description: Retrieves the size, in bytes, of a specified stream.
helpviewer_keywords: ["IStream_Size","IStream_Size function [Windows Shell]","_win32_IStream_Size","shell.IStream_Size","shlwapi/IStream_Size"]
old-location: shell\IStream_Size.htm
tech.root: shell
ms.assetid: 93c7c24d-6431-4859-b0b8-b36392bc5108
ms.date: 12/05/2018
ms.keywords: IStream_Size, IStream_Size function [Windows Shell], _win32_IStream_Size, shell.IStream_Size, shlwapi/IStream_Size
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
 - IStream_Size
 - shlwapi/IStream_Size
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
 - IStream_Size
---

# IStream_Size function


## -description

Retrieves the size, in bytes, of a specified stream.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of the stream whose size is to be determined.

### -param pui [out]

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a>*</b>

A pointer to a <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a> structure to receive the size of the stream.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> on success or a COM failure code otherwise. See <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> for further discussion of possible error codes.

## -remarks

This function gets the size of the stream by calling the specified stream object's <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> method. It then copies the value of the <b>cbSize</b> member of the <a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure returned by <b>IStream::Stat</b> to the <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a> structure pointed to by <i>pui</i>.  If the function fails, the contents of the <b>ULARGE_INTEGER</b> structure are undefined.