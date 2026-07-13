---
UID: NF:setupapi.SetupGetSourceFileSizeW
title: SetupGetSourceFileSizeW function (setupapi.h)
description: The SetupGetSourceFileSize function reads the uncompressed size of a source file listed in an INF file. (Unicode)
helpviewer_keywords: ["SetupGetSourceFileSize", "SetupGetSourceFileSize function [Setup API]", "SetupGetSourceFileSizeW", "_setupapi_setupgetsourcefilesize", "setup.setupgetsourcefilesize", "setupapi/SetupGetSourceFileSize", "setupapi/SetupGetSourceFileSizeW"]
old-location: setup\setupgetsourcefilesize.htm
tech.root: setup
ms.assetid: f1db8ad5-b133-410e-9843-38b09e2ef5e7
ms.date: 12/05/2018
ms.keywords: SetupGetSourceFileSize, SetupGetSourceFileSize function [Setup API], SetupGetSourceFileSizeA, SetupGetSourceFileSizeW, _setupapi_setupgetsourcefilesize, setup.setupgetsourcefilesize, setupapi/SetupGetSourceFileSize, setupapi/SetupGetSourceFileSizeA, setupapi/SetupGetSourceFileSizeW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetSourceFileSizeW (Unicode) and SetupGetSourceFileSizeA (ANSI)
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
 - SetupGetSourceFileSizeW
 - setupapi/SetupGetSourceFileSizeW
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
 - SetupGetSourceFileSize
 - SetupGetSourceFileSizeA
 - SetupGetSourceFileSizeW
---

# SetupGetSourceFileSizeW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetSourceFileSize</b> function reads the uncompressed size of a source file listed in an INF file.

## -parameters

### -param InfHandle [in]

Handle to the loaded INF file that contains the <b>SourceDisksNames</b> and <b>SourceDisksFiles</b> sections. If platform-specific sections exist for the user's system (for example, <b>SourceDisksNames.x86</b> and <b>SourceDisksFiles.x86</b>), the platform-specific section will be used.

### -param InfContext [in]

Optional pointer to a context for a line in a <b>Copy Files</b> section for which the size is to be retrieved. If <i>InfContext</i> is <b>NULL</b>, the <i>FileName</i> parameter is used.

### -param FileName [in]

Optional pointer to a <b>null</b>-terminated string containing the filename (no path) for which to return the size. If this parameter is <b>NULL</b> as well as <i>InfContext</i>, then the <i>Section</i> parameter is used.

### -param Section [in]

Optional pointer to a <b>null</b>-terminated string containing the name of a <b>Copy Files</b> section. If this parameter is specified, the total size of all files listed in the section is computed.

### -param FileSize [in, out]

Pointer to a variable that receives the size, in bytes, of the specified file(s).

### -param RoundingFactor [in]

Optional value for rounding file sizes. All file sizes are rounded up to a multiple of this number before being added to the total size. Rounding is useful for more exact determinations of the space that a file will occupy on a given volume, because it allows the caller to have file sizes rounded up to a multiple of the cluster size. Rounding does not occur unless <i>RoundingFactor</i> is specified.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

One and only one of the optional parameters, <i>InfContext</i>, <i>FileName</i>, and <i>Section</i>, must be specified.





> [!NOTE]
> The setupapi.h header defines SetupGetSourceFileSize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilelocationa">SetupGetSourceFileLocation</a>
