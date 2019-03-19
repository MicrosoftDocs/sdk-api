---
UID: NF:setupapi.SetupGetLineByIndexA
title: SetupGetLineByIndexA function (setupapi.h)
author: windows-sdk-content
description: The SetupGetLineByIndex function locates a line by its index value in the specified section in the INF file.
old-location: setup\setupgetlinebyindex.htm
tech.root: SetupApi
ms.assetid: 7a1c313b-3150-4f4f-a1e9-0fc9544b97ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupGetLineByIndex, SetupGetLineByIndex function [Setup API], SetupGetLineByIndexA, SetupGetLineByIndexW, _setupapi_setupgetlinebyindex, setup.setupgetlinebyindex, setupapi/SetupGetLineByIndex, setupapi/SetupGetLineByIndexA, setupapi/SetupGetLineByIndexW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupGetLineByIndexA function


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
      call to <a href="https://msdn.microsoft.com/08c98745-ecbd-47b4-9d73-2d6765285bae">SetupGetLineCount</a>.


### -param Context [in, out]

Pointer to a variable that receives the context information for the found line.


## -returns



If the function succeeds, the return value is a nonzero value. If the function fails, the return value is 
       zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <i>InfHandle</i> references multiple INF files that have been appended together using 
    <a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>, this function 
    searches across the specified section in all files referenced by the HINF to locate the indexed line.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a>



<a href="https://msdn.microsoft.com/ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d">SetupFindNextLine</a>



<a href="https://msdn.microsoft.com/c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73">SetupFindNextMatchLine</a>
 

 

