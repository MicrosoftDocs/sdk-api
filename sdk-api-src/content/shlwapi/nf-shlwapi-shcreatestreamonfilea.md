---
UID: NF:shlwapi.SHCreateStreamOnFileA
title: SHCreateStreamOnFileA function (shlwapi.h)
description: SHCreateStreamOnFile may be altered or unavailable. Instead, use SHCreateStreamOnFileEx. (ANSI)
helpviewer_keywords: ["SHCreateStreamOnFileA", "shlwapi/SHCreateStreamOnFileA"]
old-location: shell\SHCreateStreamOnFile.htm
tech.root: shell
ms.assetid: 9b1fd6c4-d7b0-40b9-bc9f-ea062a1079c1
ms.date: 12/05/2018
ms.keywords: SHCreateStreamOnFile, SHCreateStreamOnFile function [Windows Shell], SHCreateStreamOnFileA, SHCreateStreamOnFileW, _win32_SHCreateStreamOnFile, shell.SHCreateStreamOnFile, shlwapi/SHCreateStreamOnFile, shlwapi/SHCreateStreamOnFileA, shlwapi/SHCreateStreamOnFileW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHCreateStreamOnFileW (Unicode) and SHCreateStreamOnFileA (ANSI)
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
 - SHCreateStreamOnFileA
 - shlwapi/SHCreateStreamOnFileA
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
 - SHCreateStreamOnFile
 - SHCreateStreamOnFileA
 - SHCreateStreamOnFileW
---

# SHCreateStreamOnFileA function


## -description

<p class="CCE_Message">[<b>SHCreateStreamOnFile</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatestreamonfileex">SHCreateStreamOnFileEx</a>.]

Opens or creates a file and retrieves a stream to read or write to that file.

## -parameters

### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the file name.

### -param grfMode [in]

Type: <b>DWORD</b>

One or more <a href="/windows/desktop/Stg/stgm-constants">STGM</a> values that are used to specify the file access mode and how the object that exposes the stream is created and deleted.

### -param ppstm [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

Receives an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface pointer for the stream associated with the file.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatestreamonfileex">SHCreateStreamOnFileEx</a> fully supports all <a href="/windows/desktop/Stg/stgm-constants">STGM</a> modes and allows the caller to specify file attributes if creating a new file.




> [!NOTE]
> The shlwapi.h header defines SHCreateStreamOnFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
