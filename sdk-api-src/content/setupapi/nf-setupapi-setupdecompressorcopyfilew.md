---
UID: NF:setupapi.SetupDecompressOrCopyFileW
title: SetupDecompressOrCopyFileW function (setupapi.h)
description: The SetupDecompressOrCopyFile function copies a file, decompressing it if necessary. (Unicode)
helpviewer_keywords: ["SetupDecompressOrCopyFile", "SetupDecompressOrCopyFile function [Setup API]", "SetupDecompressOrCopyFileW", "_setupapi_setupdecompressorcopyfile", "setup.setupdecompressorcopyfile", "setupapi/SetupDecompressOrCopyFile", "setupapi/SetupDecompressOrCopyFileW"]
old-location: setup\setupdecompressorcopyfile.htm
tech.root: setup
ms.assetid: 6058567b-fa34-472b-91d8-3c5f9ee741b1
ms.date: 12/05/2018
ms.keywords: SetupDecompressOrCopyFile, SetupDecompressOrCopyFile function [Setup API], SetupDecompressOrCopyFileA, SetupDecompressOrCopyFileW, _setupapi_setupdecompressorcopyfile, setup.setupdecompressorcopyfile, setupapi/SetupDecompressOrCopyFile, setupapi/SetupDecompressOrCopyFileA, setupapi/SetupDecompressOrCopyFileW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDecompressOrCopyFileW (Unicode) and SetupDecompressOrCopyFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDecompressOrCopyFileW
 - setupapi/SetupDecompressOrCopyFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDecompressOrCopyFile
 - SetupDecompressOrCopyFileA
 - SetupDecompressOrCopyFileW
---

# SetupDecompressOrCopyFileW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupDecompressOrCopyFile</b> function copies a file, decompressing it if necessary.

If a file is copied, the caller of this function is required have privileges to write into the target directory.

## -parameters

### -param SourceFileName [in]

File name of the file to be copied. You should use a <b>null</b>-terminated string. This parameter can be <b>NULL</b>. If <i>CompressionType</i> is not specified and the 
<b>SetupDecompressOrCopyFile</b> function does not find the file specified in <i>SourceFileName</i>, the function searches for the file with up to two alternate, "compressed-form" names. For example, if the file is F:\x86\cmd.exe and it is not found, the function searches for F:\x86\cmd.ex_ and, if that is not found, F:\x86\cmd.ex$ is searched for. If <i>CompressionType</i> is specified, no additional processing is performed on the filename; the file must exist exactly as specified or the function fails.

### -param TargetFileName [in]

Exact name of the target file that will be created by decompressing or copying the source file. You should use a <b>null</b>-terminated string.

### -param CompressionType [in]

Optional pointer to the compression type used on the source file. You can determine the compression type by calling 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetfilecompressioninfoa">SetupGetFileCompressionInfo</a>. If this value is FILE_COMPRESSION_NONE, the file is copied (not decompressed) regardless of any compression in use on the source. If <i>CompressionType</i> is not specified, this routine determines the compression type automatically.

## -returns

The 
<b>SetupDecompressOrCopyFile</b> function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> that indicates the outcome of the operation. 

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetfilecompressioninfoa">SetupGetFileCompressionInfo</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDecompressOrCopyFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
