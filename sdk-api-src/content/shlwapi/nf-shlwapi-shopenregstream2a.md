---
UID: NF:shlwapi.SHOpenRegStream2A
title: SHOpenRegStream2A function (shlwapi.h)
description: Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes SHOpenRegStream. (ANSI)
helpviewer_keywords: ["SHOpenRegStream2A", "STGM_READ", "STGM_READWRITE", "STGM_WRITE", "shlwapi/SHOpenRegStream2A"]
old-location: shell\SHOpenRegStream2.htm
tech.root: shell
ms.assetid: 2450dde0-cd02-4d48-be40-467b4b8be240
ms.date: 12/05/2018
ms.keywords: SHOpenRegStream2, SHOpenRegStream2 function [Windows Shell], SHOpenRegStream2A, SHOpenRegStream2W, STGM_READ, STGM_READWRITE, STGM_WRITE, _win32_SHOpenRegStream2, shell.SHOpenRegStream2, shlwapi/SHOpenRegStream2, shlwapi/SHOpenRegStream2A, shlwapi/SHOpenRegStream2W
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHOpenRegStream2W (Unicode) and SHOpenRegStream2A (ANSI)
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
 - SHOpenRegStream2A
 - shlwapi/SHOpenRegStream2A
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
 - SHOpenRegStream2
 - SHOpenRegStream2A
 - SHOpenRegStream2W
---

# SHOpenRegStream2A function


## -description

Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shopenregstreama">SHOpenRegStream</a>.

## -parameters

### -param hkey [in]

Type: <b>HKEY</b>

Required. The subtree, such as HKEY_LOCAL_MACHINE, that contains the value.

### -param pszSubkey [in, optional]

Type: <b>LPCTSTR</b>

Optional. Pointer to a null-terminated string that specifies the subkey that contains the value. This value can be <b>NULL</b>.

### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that specifies the value to be accessed. This value can be <b>NULL</b>.

### -param grfMode [in]

Type: <b>DWORD</b>

The type of access for the stream. This can be one of the following values:



#### STGM_READ

Open the stream for reading.



#### STGM_WRITE

Open the stream for writing.



#### STGM_READWRITE

Open the stream for reading and writing.

## -returns

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Returns an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface pointer if successful; otherwise, <b>NULL</b>. A <b>NULL</b> value can be caused by several situations, including an invalid <i>hkey</i> or <i>pszSubkey</i>, a subkey named by <i>pszSubkey</i> that does not exist, a caller without sufficient permissions to access the subkey, or an inability to open the stream.

## -remarks

The calling application is responsible for calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method of the returned object when that <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object is no longer needed.




> [!NOTE]
> The shlwapi.h header defines SHOpenRegStream2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
