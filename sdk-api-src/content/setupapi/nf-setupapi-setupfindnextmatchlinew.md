---
UID: NF:setupapi.SetupFindNextMatchLineW
title: SetupFindNextMatchLineW function (setupapi.h)
author: windows-sdk-content
description: The SetupFindNextMatchLine function returns the location of the next line in an INF file relative to ContextIn.Line that matches a specified key.
old-location: setup\setupfindnextmatchline.htm
tech.root: SetupApi
ms.assetid: c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupFindNextMatchLine, SetupFindNextMatchLine function [Setup API], SetupFindNextMatchLineA, SetupFindNextMatchLineW, _setupapi_setupfindnextmatchline, setup.setupfindnextmatchline, setupapi/SetupFindNextMatchLine, setupapi/SetupFindNextMatchLineA, setupapi/SetupFindNextMatchLineW
ms.topic: function
f1_keywords: 
 - "setupapi/SetupFindNextMatchLine"
dev_langs:
 - c++
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupFindNextMatchLineW (Unicode) and SetupFindNextMatchLineA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupFindNextMatchLine
 - SetupFindNextMatchLineA
 - SetupFindNextMatchLineW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupFindNextMatchLineW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFindNextMatchLine</b> function returns the location of the next line in an INF file relative to <i>ContextIn.Line</i> that matches a specified key.


## -parameters




### -param ContextIn [in]

Pointer to an INF file context, as retrieved by a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a> function.


### -param Key [in]

If this optional parameter is specified, it supplies a key to match. This parameter should be a null-terminated string. This parameter can be Null. If <i>Key</i> is not specified, the 
<b>SetupFindNextMatchLine</b> function is equivalent to the 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindnextline">SetupFindNextLine</a> function.


### -param ContextOut [in, out]

Pointer to a variable in which this function returns the context of the found line. <i>ContextOut</i> can point to <i>ContextIn</i> if the caller wishes.


## -returns



The function returns a nonzero value if it finds a matching line. Otherwise, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If <i>ContextIn.Inf</i> references multiple INF files that have been appended together using 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>, the 
<b>SetupFindNextMatchLine</b> function searches across the specified section in all files referenced by the HINF to locate the next matching line.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindnextline">SetupFindNextLine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetlinebyindexa">SetupGetLineByIndex</a>
 

 

