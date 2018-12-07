---
UID: NF:setupapi.SetupTerminateFileLog
title: SetupTerminateFileLog function
author: windows-sdk-content
description: The SetupTerminateFileLog function releases resources associated with a file log.
old-location: setup\setupterminatefilelog.htm
tech.root: SetupApi
ms.assetid: a230063a-2b4a-4ed3-8624-4859a17f8ccc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupTerminateFileLog, SetupTerminateFileLog function [Setup API], _setupapi_setupterminatefilelog, setup.setupterminatefilelog, setupapi/SetupTerminateFileLog
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
 - SetupTerminateFileLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupTerminateFileLog function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupTerminateFileLog</b> function releases resources associated with a file log.


## -parameters




### -param FileLogHandle [in]

Handle to the log file as returned by a call to 
<a href="https://msdn.microsoft.com/fac7abac-76a9-456a-843a-e1048df268b7">SetupInitializeFileLog</a>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/fac7abac-76a9-456a-843a-e1048df268b7">SetupInitializeFileLog</a>



<a href="https://msdn.microsoft.com/bc738212-ff81-4b52-b2ef-50aabf6658ab">SetupLogFile</a>
 

 

