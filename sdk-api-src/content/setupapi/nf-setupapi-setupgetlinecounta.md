---
UID: NF:setupapi.SetupGetLineCountA
title: SetupGetLineCountA function (setupapi.h)
description: The SetupGetLineCount function returns the number of lines in a specified section of an INF file. (ANSI)
helpviewer_keywords: ["SetupGetLineCountA", "setupapi/SetupGetLineCountA"]
old-location: setup\setupgetlinecount.htm
tech.root: setup
ms.assetid: 08c98745-ecbd-47b4-9d73-2d6765285bae
ms.date: 12/05/2018
ms.keywords: SetupGetLineCount, SetupGetLineCount function [Setup API], SetupGetLineCountA, SetupGetLineCountW, _setupapi_setupgetlinecount, setup.setupgetlinecount, setupapi/SetupGetLineCount, setupapi/SetupGetLineCountA, setupapi/SetupGetLineCountW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetLineCountW (Unicode) and SetupGetLineCountA (ANSI)
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
 - SetupGetLineCountA
 - setupapi/SetupGetLineCountA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupGetLineCount
 - SetupGetLineCountA
 - SetupGetLineCountW
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupGetLineCountA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetLineCount</b> function returns the number of lines in a specified section of an INF file.

## -parameters

### -param InfHandle [in]

Handle to the INF file.

### -param Section [in]

Pointer to a null-terminated string that specifies the section in which you want to count the lines.

## -returns

If <i>InfHandle</i> references multiple INF files that have been appended  using 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>, this function returns the sum of the lines in all of the INF files containing the specified section. A return value of 0 specifies an empty section. If the section does not exist, the function returns –1.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupGetLineCount as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
