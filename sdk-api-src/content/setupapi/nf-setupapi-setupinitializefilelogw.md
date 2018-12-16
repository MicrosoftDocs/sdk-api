---
UID: NF:setupapi.SetupInitializeFileLogW
title: SetupInitializeFileLogW function
author: windows-sdk-content
description: The SetupInitializeFileLog function initializes a file to record installation operations and outcomes. This can be the system log, where the system tracks the files installed as part of Windows, or any other file.
old-location: setup\setupinitializefilelog.htm
tech.root: SetupApi
ms.assetid: fac7abac-76a9-456a-843a-e1048df268b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupInitializeFileLog, SetupInitializeFileLog function [Setup API], SetupInitializeFileLogA, SetupInitializeFileLogW, _setupapi_setupinitializefilelog, setup.setupinitializefilelog, setupapi/SetupInitializeFileLog, setupapi/SetupInitializeFileLogA, setupapi/SetupInitializeFileLogW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupInitializeFileLogW (Unicode) and SetupInitializeFileLogA (ANSI)
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
 - SetupInitializeFileLog
 - SetupInitializeFileLogA
 - SetupInitializeFileLogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupInitializeFileLogW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupInitializeFileLog</b> function initializes a file to record installation operations and outcomes. This can be the system log, where the system tracks the files installed as part of Windows, or any other file.


## -parameters




### -param LogFileName [in]

Optional pointer to the file name of the file to use as the log file. You should use a <b>null</b>-terminated string. The <i>LogFileName</i> parameter must be specified if <i>Flags</i> does not include SPFILELOG_SYSTEMLOG. The <i>LogFileName</i> parameter must not be specified if <i>Flags</i> includes SPFILELOG_SYSTEMLOG. This parameter can be <b>NULL</b>.


### -param Flags [in]

Controls the log file initialization. This parameter can be a combination of the following values. 







#### SPFILELOG_SYSTEMLOG

Use the system file log. The user must be an Administrator to specify this option unless SPFILELOG_QUERYONLY is specified and <i>LogFileName</i> is not specified. Do not specify SPFILELOG_SYSTEMLOG in combination with SPFILELOG_FORCENEW.



#### SPFILELOG_FORCENEW

If the log file exists, overwrite it. If the log file exists and this flag is not specified, any new files that are installed are added to the list in the existing log file. Do not specify in combination with SPFILELOG_SYSTEMLOG.



#### SPFILELOG_QUERYONLY

Open the log file for querying only.


##### - Flags.SPFILELOG_FORCENEW

If the log file exists, overwrite it. If the log file exists and this flag is not specified, any new files that are installed are added to the list in the existing log file. Do not specify in combination with SPFILELOG_SYSTEMLOG.


##### - Flags.SPFILELOG_QUERYONLY

Open the log file for querying only.


##### - Flags.SPFILELOG_SYSTEMLOG

Use the system file log. The user must be an Administrator to specify this option unless SPFILELOG_QUERYONLY is specified and <i>LogFileName</i> is not specified. Do not specify SPFILELOG_SYSTEMLOG in combination with SPFILELOG_FORCENEW.


## -returns



The function returns the handle to the log file if it is successful. Otherwise, the return value is INVALID_HANDLE_VALUE and the logged error can be retrieved by a call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/bc738212-ff81-4b52-b2ef-50aabf6658ab">SetupLogFile</a>



<a href="https://msdn.microsoft.com/a230063a-2b4a-4ed3-8624-4859a17f8ccc">SetupTerminateFileLog</a>
 

 

