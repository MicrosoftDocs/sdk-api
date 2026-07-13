---
UID: NF:setupapi.SetupInitializeFileLogW
title: SetupInitializeFileLogW function (setupapi.h)
description: The SetupInitializeFileLog function initializes a file to record installation operations and outcomes. This can be the system log, where the system tracks the files installed as part of Windows, or any other file. (Unicode)
helpviewer_keywords: ["SetupInitializeFileLog", "SetupInitializeFileLog function [Setup API]", "SetupInitializeFileLogW", "_setupapi_setupinitializefilelog", "setup.setupinitializefilelog", "setupapi/SetupInitializeFileLog", "setupapi/SetupInitializeFileLogW"]
old-location: setup\setupinitializefilelog.htm
tech.root: setup
ms.assetid: fac7abac-76a9-456a-843a-e1048df268b7
ms.date: 12/05/2018
ms.keywords: SetupInitializeFileLog, SetupInitializeFileLog function [Setup API], SetupInitializeFileLogA, SetupInitializeFileLogW, _setupapi_setupinitializefilelog, setup.setupinitializefilelog, setupapi/SetupInitializeFileLog, setupapi/SetupInitializeFileLogA, setupapi/SetupInitializeFileLogW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupInitializeFileLogW
 - setupapi/SetupInitializeFileLogW
dev_langs:
 - c++
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuplogfilea">SetupLogFile</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupterminatefilelog">SetupTerminateFileLog</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupInitializeFileLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
