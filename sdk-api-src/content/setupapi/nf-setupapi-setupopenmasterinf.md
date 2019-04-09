---
UID: NF:setupapi.SetupOpenMasterInf
title: SetupOpenMasterInf function (setupapi.h)
author: windows-sdk-content
description: The SetupOpenMasterInf function opens the master INF file that contains file and layout information for files shipped with Windows.
old-location: setup\setupopenmasterinf.htm
tech.root: SetupApi
ms.assetid: dbf3fb81-7416-4eb7-95b9-adfc17b2a364
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupOpenMasterInf, SetupOpenMasterInf function [Setup API], _setupapi_setupopenmasterinf, setup.setupopenmasterinf, setupapi/SetupOpenMasterInf
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
 - SetupOpenMasterInf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupOpenMasterInf function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenMasterInf</b> function opens the master INF file that contains file and layout information for files shipped with Windows.


## -parameters






## -returns



If 
<b>SetupOpenMasterInf</b> is successful, it returns a handle to the opened INF file that contains file/layout information for files shipped with Windows. Otherwise, the return value is INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>



<a href="https://msdn.microsoft.com/a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7">SetupOpenInfFile</a>
 

 

