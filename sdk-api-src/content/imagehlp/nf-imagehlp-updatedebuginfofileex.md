---
UID: NF:imagehlp.UpdateDebugInfoFileEx
title: UpdateDebugInfoFileEx function (imagehlp.h)
description: Uses the specified extended information to update the corresponding fields in the symbol file.
helpviewer_keywords: ["UpdateDebugInfoFileEx","UpdateDebugInfoFileEx function","_win32_updatedebuginfofileex","base.updatedebuginfofileex","imagehlp/UpdateDebugInfoFileEx"]
old-location: base\updatedebuginfofileex.htm
tech.root: Debug
ms.assetid: 67da28db-1566-4d12-8090-9f38fdfd246e
ms.date: 12/05/2018
ms.keywords: UpdateDebugInfoFileEx, UpdateDebugInfoFileEx function, _win32_updatedebuginfofileex, base.updatedebuginfofileex, imagehlp/UpdateDebugInfoFileEx
req.header: imagehlp.h
req.include-header: 
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
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UpdateDebugInfoFileEx
 - imagehlp/UpdateDebugInfoFileEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - UpdateDebugInfoFileEx
---

# UpdateDebugInfoFileEx function


## -description

Uses the specified extended information to update the corresponding fields in the symbol file.
<div class="alert"><b>Note</b>  This function works with .dbg files, not .pdb files.</div><div> </div>

## -parameters

### -param ImageFileName [in]

The name of the image that is now out of date with respect to its symbol file.

### -param SymbolPath [in]

The path in which to look for the symbol file.

### -param DebugFilePath [out]

 A pointer to a buffer that receives the name of the symbol file that was updated.

### -param NtHeaders [in]

A pointer to an 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure that specifies the new header information.

### -param OldCheckSum [in]

The original checksum value. If this value does not match the checksum that is present in the mapped image, the flags in the symbol file contain IMAGE_SEPARATE_DEBUG_MISMATCH and the last error value is set to ERROR_INVALID_DATA.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

The 
<b>UpdateDebugInfoFileEx</b> function takes the information stored in the 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure and updates the corresponding fields in the symbol file. Any time an image file is modified, this function should be called to keep the numbers in sync. Specifically, whenever an image checksum changes, the symbol file should be updated to match.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>