---
UID: NF:setupapi.SetupCloseInfFile
title: SetupCloseInfFile function
author: windows-driver-content
description: The SetupCloseInfFile function closes the INF file opened by a call to SetupOpenInfFile. This function closes any INF files appended to it by calling SetupOpenAppendInfFile.
old-location: setup\setupcloseinffile.htm
old-project: SetupApi
ms.assetid: 78b6a69d-e588-45f1-bf5c-a6feaf8b3364
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupCloseInfFile, SetupCloseInfFile function [Setup API], _setupapi_setupcloseinffile, setup.setupcloseinffile, setupapi/SetupCloseInfFile
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
-	SetupCloseInfFile
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupCloseInfFile function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCloseInfFile</b> function closes the INF file opened by a call to 
<a href="https://msdn.microsoft.com/a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7">SetupOpenInfFile</a>. This function closes any INF files appended to it by 
calling <a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>.


## -parameters




### -param InfHandle [in]

Handle to the INF file to be closed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>



<a href="https://msdn.microsoft.com/a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7">SetupOpenInfFile</a>
 

 

