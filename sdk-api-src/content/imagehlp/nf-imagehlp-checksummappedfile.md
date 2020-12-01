---
UID: NF:imagehlp.CheckSumMappedFile
title: CheckSumMappedFile function (imagehlp.h)
description: Computes the checksum of the specified image file.
helpviewer_keywords: ["CheckSumMappedFile","CheckSumMappedFile function","_win32_checksummappedfile","base.checksummappedfile","imagehlp/CheckSumMappedFile"]
old-location: base\checksummappedfile.htm
tech.root: Debug
ms.assetid: 01a99601-64de-412d-991e-b1708286ca8c
ms.date: 12/05/2018
ms.keywords: CheckSumMappedFile, CheckSumMappedFile function, _win32_checksummappedfile, base.checksummappedfile, imagehlp/CheckSumMappedFile
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
 - CheckSumMappedFile
 - imagehlp/CheckSumMappedFile
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
 - CheckSumMappedFile
---

# CheckSumMappedFile function


## -description

Computes the checksum of the specified image file.

## -parameters

### -param BaseAddress [in]

The base address of the mapped file. This value is obtained by calling the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.

### -param FileLength [in]

The size of the file, in bytes.

### -param HeaderSum [out]

A pointer to a variable that receives the original checksum from the image file, or zero if there is an error.

### -param CheckSum [out]

A pointer to the variable that receives the computed checksum.

## -returns

If the function succeeds, the return value is a pointer to the 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure contained in the mapped image.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>CheckSumMappedFile</b> function computes a new checksum for the file and returns it in the <i>CheckSum</i> parameter. This function is used by any application that creates or modifies an executable image. Checksums are required for kernel-mode drivers and some system DLLs. The linker computes the original checksum at link time, if you use the appropriate linker switch. For more details, see your linker documentation.

It is recommended that all images have valid checksums. It is the caller's responsibility to place the newly computed checksum into the mapped image and update the on-disk image of the file.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma">MapFileAndCheckSum</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>