---
UID: NF:setupapi.SetupFindNextMatchLineW
title: SetupFindNextMatchLineW function
author: windows-sdk-content
description: The SetupFindNextMatchLine function returns the location of the next line in an INF file relative to ContextIn.Line that matches a specified key.
old-location: setup\setupfindnextmatchline.htm
old-project: SetupApi
ms.assetid: c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetupFindNextMatchLine, SetupFindNextMatchLine function [Setup API], SetupFindNextMatchLineA, SetupFindNextMatchLineW, _setupapi_setupfindnextmatchline, setup.setupfindnextmatchline, setupapi/SetupFindNextMatchLine, setupapi/SetupFindNextMatchLineA, setupapi/SetupFindNextMatchLineW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
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
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupFindNextMatchLineW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFindNextMatchLine</b> function returns the location of the next line in an INF file relative to <i>ContextIn.Line</i> that matches a specified key.


## -parameters




### -param ContextIn [in]

Pointer to an INF file context, as retrieved by a call to the 
<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a> function.


### -param Key [in]

If this optional parameter is specified, it supplies a key to match. This parameter should be a null-terminated string. This parameter can be Null. If <i>Key</i> is not specified, the 
<b>SetupFindNextMatchLine</b> function is equivalent to the 
<a href="https://msdn.microsoft.com/ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d">SetupFindNextLine</a> function.


### -param ContextOut [in, out]

Pointer to a variable in which this function returns the context of the found line. <i>ContextOut</i> can point to <i>ContextIn</i> if the caller wishes.


## -returns



The function returns a nonzero value if it finds a matching line. Otherwise, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <i>ContextIn.Inf</i> references multiple INF files that have been appended together using 
<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>, the 
<b>SetupFindNextMatchLine</b> function searches across the specified section in all files referenced by the HINF to locate the next matching line.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a>



<a href="https://msdn.microsoft.com/ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d">SetupFindNextLine</a>



<a href="https://msdn.microsoft.com/7a1c313b-3150-4f4f-a1e9-0fc9544b97ab">SetupGetLineByIndex</a>
 

 

