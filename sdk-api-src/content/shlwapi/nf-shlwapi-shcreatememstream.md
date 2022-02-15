---
UID: NF:shlwapi.SHCreateMemStream
title: SHCreateMemStream function (shlwapi.h)
description: Creates a memory stream using a similar process to CreateStreamOnHGlobal.
helpviewer_keywords: ["SHCreateMemStream","SHCreateMemStream function [Windows Shell]","_win32_SHCreateMemStream","shell.SHCreateMemStream","shlwapi/SHCreateMemStream"]
old-location: shell\SHCreateMemStream.htm
tech.root: shell
ms.assetid: f3ae8241-f3a6-4007-a10f-ff05960c5de8
ms.date: 12/05/2018
ms.keywords: SHCreateMemStream, SHCreateMemStream function [Windows Shell], _win32_SHCreateMemStream, shell.SHCreateMemStream, shlwapi/SHCreateMemStream
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateMemStream
 - shlwapi/SHCreateMemStream
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
 - SHCreateMemStream
---

# SHCreateMemStream function


## -description

Creates a memory stream using a similar process to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a>.

## -parameters

### -param pInit [in, optional]

Type: <b>const BYTE*</b>

A pointer to a buffer of size <i>cbInit</i>. The contents of this buffer are used to set the initial contents of the memory stream. If this parameter is <b>NULL</b>, the returned memory stream does not have any initial content.

### -param cbInit [in]

Type: <b>UINT</b>

The number of bytes in the buffer pointed to by <i>pInit</i>. If <i>pInit</i> is set to <b>NULL</b>, <i>cbInit</i> must be zero.

## -returns

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

On success, returns a pointer to the created memory stream. Returns <b>NULL</b> if the stream object could not be allocated.

## -remarks

Prior to Windows Vista, this function was not included in the public Shlwapi.h file, nor was it exported by name from Shlwapi.dll. To use it on earlier systems, you must call it directly from the Shlwapi.dll file as ordinal 12.

This function creates a memory stream. This is an implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface that stores its contents in memory. <b>SHCreateMemStream</b> differs from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> in the following ways.

                

<ul>
<li>Thread safety. The stream created by <b>SHCreateMemStream</b> is thread-safe as of Windows 8. On earlier systems, the stream is not thread-safe. The stream created by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> is thread-safe.</li>
<li>Initial contents. <b>SHCreateMemStream</b> accepts the initial contents in the form of a buffer. <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> accepts the initial contents in the form of an HGLOBAL.</li>
<li>Access to contents. <b>SHCreateMemStream</b> does not allow direct access to the stream contents. <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> permits access through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream">GetHGlobalFromStream</a>.</li>
<li>Failure information. If <b>SHCreateMemStream</b> returns <b>NULL</b>, it was unable to allocate the necessary memory. Callers should assume the cause is E_OUTOFMEMORY.</li>
<li>Support for <a href="/windows/desktop/api/objidl/nf-objidl-istream-clone">IStream::Clone</a>. Prior to Windows 8, the stream created by <b>SHCreateMemStream</b> does not support <b>IStream::Clone</b>. The stream created by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> does. As of Windows 8, the stream created by <b>SHCreateMemStream</b> does support <b>IStream::Clone</b>.</li>
<li>The stream returned by <b>SHCreateMemStream</b> returns S_FALSE from <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">IStream::Read</a> if you attempt to read past the end of the buffer. The stream returned by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> returns S_OK and sets *pcbRead to 0 if you attempt to read past the end of the buffer.</li>
</ul>