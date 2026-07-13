---
UID: NF:setupapi.SetupFindFirstLineW
title: SetupFindFirstLineW function (setupapi.h)
description: The SetupFindFirstLine function locates a line in the specified section of an INF file. If the Key parameter is NULL, SetupFindFirstLine returns the first line of the section. (Unicode)
helpviewer_keywords: ["SetupFindFirstLine", "SetupFindFirstLine function [Setup API]", "SetupFindFirstLineW", "_setupapi_setupfindfirstline", "setup.setupfindfirstline", "setupapi/SetupFindFirstLine", "setupapi/SetupFindFirstLineW"]
old-location: setup\setupfindfirstline.htm
tech.root: setup
ms.assetid: ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b
ms.date: 12/05/2018
ms.keywords: SetupFindFirstLine, SetupFindFirstLine function [Setup API], SetupFindFirstLineA, SetupFindFirstLineW, _setupapi_setupfindfirstline, setup.setupfindfirstline, setupapi/SetupFindFirstLine, setupapi/SetupFindFirstLineA, setupapi/SetupFindFirstLineW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupFindFirstLineW (Unicode) and SetupFindFirstLineA (ANSI)
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
 - SetupFindFirstLineW
 - setupapi/SetupFindFirstLineW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-setupapi-inf-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupFindFirstLine
 - SetupFindFirstLineA
 - SetupFindFirstLineW
req.apiset: ext-ms-win-setupapi-inf-l1-1-0 (introduced in Windows 8)
---

# SetupFindFirstLineW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFindFirstLine</b> function locates a line in the specified section of an INF file. If the <i>Key</i> parameter is <b>NULL</b>, 
<b>SetupFindFirstLine</b> returns the first line of the section.

## -parameters

### -param InfHandle [in]

Handle to the INF file to query.

### -param Section [in]

Pointer to a <b>null</b>-terminated string specifying the section of the INF files to search in.

### -param Key [in]

Optional pointer to a <b>null</b>-terminated string specifying the key to search for within the section. The <b>null</b>-terminated string should not exceed the size of the destination buffer. This parameter can be <b>NULL</b>. If <i>Key</i> is <b>NULL</b>, the first line in the section is returned.

### -param Context [in, out]

Pointer to a structure that receives the context information used internally by the INF handle. Applications must not overwrite values in this structure.

## -returns

If the function could not find a line, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>InfHandle</i> parameter references multiple INF files that have been appended together using 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>, the 
<b>SetupFindFirstLine</b> function searches across the specified section in all of the files referenced by the specified HINF.





> [!NOTE]
> The setupapi.h header defines SetupFindFirstLine as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextline">SetupFindNextLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextmatchlinea">SetupFindNextMatchLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetlinebyindexa">SetupGetLineByIndex</a>
