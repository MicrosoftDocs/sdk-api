---
UID: NF:shlwapi.SHOpenRegStreamA
title: SHOpenRegStreamA function (shlwapi.h)
description: Deprecated. (SHOpenRegStreamA)
helpviewer_keywords: ["SHOpenRegStreamA", "STGM_READ", "STGM_READWRITE", "STGM_WRITE", "shlwapi/SHOpenRegStreamA"]
old-location: shell\SHOpenRegStream.htm
tech.root: shell
ms.assetid: 2f839b89-8584-4b4d-91e7-166b6e2b6892
ms.date: 12/05/2018
ms.keywords: SHOpenRegStream, SHOpenRegStream function [Windows Shell], SHOpenRegStreamA, SHOpenRegStreamW, STGM_READ, STGM_READWRITE, STGM_WRITE, _win32_SHOpenRegStream, shell.SHOpenRegStream, shlwapi/SHOpenRegStream, shlwapi/SHOpenRegStreamA, shlwapi/SHOpenRegStreamW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHOpenRegStreamW (Unicode) and SHOpenRegStreamA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHOpenRegStreamA
 - shlwapi/SHOpenRegStreamA
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
 - SHOpenRegStream
 - SHOpenRegStreamA
 - SHOpenRegStreamW
---

# SHOpenRegStreamA function


## -description

Deprecated. Opens a registry value and supplies a stream that can be used to read from or write to the value.

            
<div class="alert"><b>Note</b>  This function has been replaced by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shopenregstream2a">SHOpenRegStream2</a>. It is recommended that you use <b>SHOpenRegStream2</b> at all times.</div><div> </div>

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

Open the stream for both reading and writing.

## -returns

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Returns an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface pointer if successful; otherwise, <b>NULL</b>. A <b>NULL</b> value can be caused by several situations, including an invalid <i>hkey</i> or <i>pszSubkey</i>, or an inability to open the stream. 

                    

<div class="alert"><b>Note</b>  In some situations, such as when the subkey named by <i>pszSubkey</i> does not exist or the caller does not have sufficient permissions to access the subkey, a zero-length stream is returned rather than a <b>NULL</b> value. <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shopenregstream2a">SHOpenRegStream2</a> returns <b>NULL</b> in all error situations and is the preferred function for that reason.</div>
<div> </div>

## -remarks

The calling application is responsible for calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method of the returned object when that <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object is no longer needed.




> [!NOTE]
> The shlwapi.h header defines SHOpenRegStream as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
