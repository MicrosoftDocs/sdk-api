---
UID: NF:setupapi.SetupFindFirstLineA
title: SetupFindFirstLineA function
author: windows-sdk-content
description: The SetupFindFirstLine function locates a line in the specified section of an INF file. If the Key parameter is NULL, SetupFindFirstLine returns the first line of the section.
old-location: setup\setupfindfirstline.htm
old-project: SetupApi
ms.assetid: ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupFindFirstLine, SetupFindFirstLine function [Setup API], SetupFindFirstLineA, SetupFindFirstLineW, _setupapi_setupfindfirstline, setup.setupfindfirstline, setupapi/SetupFindFirstLine, setupapi/SetupFindFirstLineA, setupapi/SetupFindFirstLineW
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
req.unicode-ansi: SetupFindFirstLineW (Unicode) and SetupFindFirstLineA (ANSI)
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
-	SetupFindFirstLine
-	SetupFindFirstLineA
-	SetupFindFirstLineW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupFindFirstLineA function


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the <i>InfHandle</i> parameter references multiple INF files that have been appended together using 
<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>, the 
<b>SetupFindFirstLine</b> function searches across the specified section in all of the files referenced by the specified HINF.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d">SetupFindNextLine</a>



<a href="https://msdn.microsoft.com/c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73">SetupFindNextMatchLine</a>



<a href="https://msdn.microsoft.com/7a1c313b-3150-4f4f-a1e9-0fc9544b97ab">SetupGetLineByIndex</a>
 

 

