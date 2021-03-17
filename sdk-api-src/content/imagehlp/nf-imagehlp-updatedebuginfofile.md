---
UID: NF:imagehlp.UpdateDebugInfoFile
title: UpdateDebugInfoFile function (imagehlp.h)
description: Uses the specified information to update the corresponding fields in the symbol file.
helpviewer_keywords: ["UpdateDebugInfoFile","UpdateDebugInfoFile function","_win32_updatedebuginfofile","base.updatedebuginfofile","imagehlp/UpdateDebugInfoFile"]
old-location: base\updatedebuginfofile.htm
tech.root: Debug
ms.assetid: b29026e2-3063-447c-9449-7105deb3d744
ms.date: 12/05/2018
ms.keywords: UpdateDebugInfoFile, UpdateDebugInfoFile function, _win32_updatedebuginfofile, base.updatedebuginfofile, imagehlp/UpdateDebugInfoFile
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
 - UpdateDebugInfoFile
 - imagehlp/UpdateDebugInfoFile
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
 - UpdateDebugInfoFile
---

# UpdateDebugInfoFile function


## -description

Uses the specified information to update the corresponding fields in the symbol file.
<div class="alert"><b>Note</b>  This function works with .dbg files, not .pdb files.</div><div> </div>This function has been superseded by the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-updatedebuginfofileex">UpdateDebugInfoFileEx</a> function. Use 
<b>UpdateDebugInfoFileEx</b> to verify the checksum value.

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

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>UpdateDebugInfoFile</b> function takes the information stored in the 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure and updates the corresponding fields in the symbol file. Any time an image file is modified, this function should be called to keep the numbers in sync. Specifically, whenever an image checksum changes, the symbol file should be updated to match.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-updatedebuginfofileex">UpdateDebugInfoFileEx</a>