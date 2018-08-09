---
UID: NF:setupapi.SetupGetLineCountA
title: SetupGetLineCountA function
author: windows-sdk-content
description: The SetupGetLineCount function returns the number of lines in a specified section of an INF file.
old-location: setup\setupgetlinecount.htm
old-project: SetupApi
ms.assetid: 08c98745-ecbd-47b4-9d73-2d6765285bae
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetupGetLineCount, SetupGetLineCount function [Setup API], SetupGetLineCountA, SetupGetLineCountW, _setupapi_setupgetlinecount, setup.setupgetlinecount, setupapi/SetupGetLineCount, setupapi/SetupGetLineCountA, setupapi/SetupGetLineCountW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
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
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
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
<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>, this function returns the sum of the lines in all of the INF files containing the specified section. A return value of 0 specifies an empty section. If the section does not exist, the function returns –1.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

