---
UID: NF:shlobj_core.OpenRegStream
title: OpenRegStream function (shlobj_core.h)
description: OpenRegStream may be altered or unavailable. Instead, use SHOpenRegStream2 or SHOpenRegStream.
helpviewer_keywords: ["OpenRegStream","OpenRegStream function [Windows Shell]","STGM_READ","STGM_READWRITE","STGM_WRITE","_win32_OpenRegStream","shell.OpenRegStream","shlobj_core/OpenRegStream"]
old-location: shell\OpenRegStream.htm
tech.root: shell
ms.assetid: e1e35c94-84ac-4aa1-b2a1-47b37a7f224e
ms.date: 12/05/2018
ms.keywords: OpenRegStream, OpenRegStream function [Windows Shell], STGM_READ, STGM_READWRITE, STGM_WRITE, _win32_OpenRegStream, shell.OpenRegStream, shlobj_core/OpenRegStream
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenRegStream
 - shlobj_core/OpenRegStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - OpenRegStream
---

# OpenRegStream function


## -description

<p class="CCE_Message">[<b>OpenRegStream</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shopenregstream2a">SHOpenRegStream2</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shopenregstreama">SHOpenRegStream</a>.]

Opens a registry value and supplies an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface that can be used to read from or write to the value.

## -parameters

### -param hkey [in]

Type: <b>HKEY</b>

A handle to the key that is currently open.

### -param pszSubkey [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that specifies the name of the subkey.

### -param pszValue [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that specifies the value to be accessed.

### -param grfMode

Type: <b>DWORD</b>

The type of access for the stream. This can be one of the following values.



#### STGM_READ

Open the stream for reading.



#### STGM_WRITE

Open the stream for writing.



#### STGM_READWRITE

Open the stream for reading and writing.

## -returns

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Returns the address of an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface if successful, or <b>NULL</b> otherwise.