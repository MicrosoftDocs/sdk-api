---
UID: NF:setupapi.SetupGetLineByIndexA
title: SetupGetLineByIndexA function (setupapi.h)
author: windows-sdk-content
description: The SetupGetLineByIndex function locates a line by its index value in the specified section in the INF file.
old-location: setup\setupgetlinebyindex.htm
tech.root: SetupApi
ms.assetid: 7a1c313b-3150-4f4f-a1e9-0fc9544b97ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupGetLineByIndex, SetupGetLineByIndex function [Setup API], SetupGetLineByIndexA, SetupGetLineByIndexW, _setupapi_setupgetlinebyindex, setup.setupgetlinebyindex, setupapi/SetupGetLineByIndex, setupapi/SetupGetLineByIndexA, setupapi/SetupGetLineByIndexW
ms.topic: function
f1_keywords: ["setupapi/SetupGetLineByIndex"]
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
ms.custom: 19H1
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
      call to <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetlinecounta">SetupGetLineCount</a>.


### -param Context [in, out]

Pointer to a variable that receives the context information for the found line.


## -returns



If the function succeeds, the return value is a nonzero value. If the function fails, the return value is 
       zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If <i>InfHandle</i> references multiple INF files that have been appended together using 
    <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>, this function 
    searches across the specified section in all files referenced by the HINF to locate the indexed line.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindnextline">SetupFindNextLine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfindnextmatchlinea">SetupFindNextMatchLine</a>
 

 

