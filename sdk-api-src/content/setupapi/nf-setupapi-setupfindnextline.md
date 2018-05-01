---
UID: NF:setupapi.SetupFindNextLine
title: SetupFindNextLine function
author: windows-driver-content
description: The SetupFindNextLine returns the location of the next line in an INF file section relative to ContextIn.Line.
old-location: setup\setupfindnextline.htm
old-project: SetupApi
ms.assetid: ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: SetupFindNextLine, SetupFindNextLine function [Setup API], _setupapi_setupfindnextline, setup.setupfindnextline, setupapi/SetupFindNextLine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
-	Ext-MS-Win-setupapi-inf-l1-1-0.dll
-	Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
-	SetupFindNextLine
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupFindNextLine function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFindNextLine</b> returns the location of the next line in an INF file section relative to <i>ContextIn.Line</i>.


## -parameters




### -param ContextIn [in]

Pointer to the INF file context retrieved by a call to the 
<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a> function.


### -param ContextOut [out]

Pointer to a variable in which this function returns the context of the found line. <i>ContextOut</i> can point to <i>ContextIn</i> if the caller wishes.


## -returns



If this function finds the next line, the return value is a nonzero value. Otherwise, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <i>ContextIn.Line</i> references multiple INF files that have been appended together using 
<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>, this function searches across the specified section in all files referenced by the HINF to locate the next line.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a>



<a href="https://msdn.microsoft.com/c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73">SetupFindNextMatchLine</a>



<a href="https://msdn.microsoft.com/7a1c313b-3150-4f4f-a1e9-0fc9544b97ab">SetupGetLineByIndex</a>
 

 

