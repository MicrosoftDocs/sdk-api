---
UID: NF:shlobj_core.SHCreateFileExtractIconA
tech.root: shell 
title: SHCreateFileExtractIconA
ms.date: 04/14/2021
targetos: Windows
description: SHCreateFileExtractIcon may be altered or unavailable. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Shell32.dll (version 5.0 or later) 
req.header: shlobj_core.h
req.idl: 
req.include-header: Shlobj.h 
req.irql: 
req.kmdf-ver: 
req.lib: Shell32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only] 
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateFileExtractIconA
 - SHCreateFileExtractIcon
f1_keywords:
 - SHCreateFileExtractIconA
 - shlobj_core/SHCreateFileExtractIconA
 - SHCreateFileExtractIcon
 - shlobj_core/SHCreateFileExtractIcon
dev_langs:
 - c++
---

# SHCreateFileExtractIconA function

## -description

<p class="CCE_Message">[<b>SHCreateFileExtractIcon</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a default <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> handler for a file system object. Namespace extensions that display file system objects typically use this function. The extension and file attributes derive all that is needed for a simple icon extractor.

## -parameters

### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the file system object. The buffer must not exceed MAX_PATH characters in length.

### -param dwFileAttributes [in]

Type: <b>DWORD</b>

A combination of one or more file attribute flags (FILE_ATTRIBUTE_* values as defined in Winnt.h) that specify the type of object.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID of the icon extractor interface to create. This must be either IID_IExtractIconA or IID_IExtractIconW.

### -param ppv

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
