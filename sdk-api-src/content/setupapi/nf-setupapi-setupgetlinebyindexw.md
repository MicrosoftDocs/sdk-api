---
UID: NF:setupapi.SetupGetLineByIndexW
title: SetupGetLineByIndexW function (setupapi.h)
description: The SetupGetLineByIndex function locates a line by its index value in the specified section in the INF file. (Unicode)
helpviewer_keywords: ["SetupGetLineByIndex", "SetupGetLineByIndex function [Setup API]", "SetupGetLineByIndexW", "_setupapi_setupgetlinebyindex", "setup.setupgetlinebyindex", "setupapi/SetupGetLineByIndex", "setupapi/SetupGetLineByIndexW"]
old-location: setup\setupgetlinebyindex.htm
tech.root: setup
ms.assetid: 7a1c313b-3150-4f4f-a1e9-0fc9544b97ab
ms.date: 12/05/2018
ms.keywords: SetupGetLineByIndex, SetupGetLineByIndex function [Setup API], SetupGetLineByIndexA, SetupGetLineByIndexW, _setupapi_setupgetlinebyindex, setup.setupgetlinebyindex, setupapi/SetupGetLineByIndex, setupapi/SetupGetLineByIndexA, setupapi/SetupGetLineByIndexW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetLineByIndexW (Unicode) and SetupGetLineByIndexA (ANSI)
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
 - SetupGetLineByIndexW
 - setupapi/SetupGetLineByIndexW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupGetLineByIndex
 - SetupGetLineByIndexA
 - SetupGetLineByIndexW
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupGetLineByIndexW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the 
    Requirements section. It may be altered or unavailable in subsequent versions. SetupAPI should no longer be used 
    for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI 
    continues to be used for installing device drivers.]

The <b>SetupGetLineByIndex</b> function locates a line by its index value in the 
    specified section in the INF file.

## -parameters

### -param InfHandle [in]

Handle to the INF file.

### -param Section [in]

Pointer to a null-terminated string specifying the section of the INF file to search.

### -param Index [in]

Index of the line to be located. The total number of lines in a particular section can be found with a 
      call to <a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetlinecounta">SetupGetLineCount</a>.

### -param Context [in, out]

Pointer to a variable that receives the context information for the found line.

## -returns

If the function succeeds, the return value is a nonzero value. If the function fails, the return value is 
       zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>InfHandle</i> references multiple INF files that have been appended together using 
    <a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>, this function 
    searches across the specified section in all files referenced by the HINF to locate the indexed line.





> [!NOTE]
> The setupapi.h header defines SetupGetLineByIndex as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextline">SetupFindNextLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextmatchlinea">SetupFindNextMatchLine</a>
