---
UID: NF:setupapi.SetupFindNextLine
title: SetupFindNextLine function (setupapi.h)
description: The SetupFindNextLine returns the location of the next line in an INF file section relative to ContextIn.Line.
helpviewer_keywords: ["SetupFindNextLine","SetupFindNextLine function [Setup API]","_setupapi_setupfindnextline","setup.setupfindnextline","setupapi/SetupFindNextLine"]
old-location: setup\setupfindnextline.htm
tech.root: setup
ms.assetid: ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d
ms.date: 12/05/2018
ms.keywords: SetupFindNextLine, SetupFindNextLine function [Setup API], _setupapi_setupfindnextline, setup.setupfindnextline, setupapi/SetupFindNextLine
req.header: setupapi.h
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupFindNextLine
 - setupapi/SetupFindNextLine
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
 - SetupFindNextLine
req.apiset: ext-ms-win-setupapi-inf-l1-1-0 (introduced in Windows 8)
---

# SetupFindNextLine function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFindNextLine</b> returns the location of the next line in an INF file section relative to <i>ContextIn.Line</i>.

## -parameters

### -param ContextIn [in]

Pointer to the INF file context retrieved by a call to the 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a> function.

### -param ContextOut [out]

Pointer to a variable in which this function returns the context of the found line. <i>ContextOut</i> can point to <i>ContextIn</i> if the caller wishes.

## -returns

If this function finds the next line, the return value is a nonzero value. Otherwise, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>ContextIn.Line</i> references multiple INF files that have been appended together using 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>, this function searches across the specified section in all files referenced by the HINF to locate the next line.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextmatchlinea">SetupFindNextMatchLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetlinebyindexa">SetupGetLineByIndex</a>
