---
UID: NF:setupapi.SetupTerminateFileLog
title: SetupTerminateFileLog function (setupapi.h)
description: The SetupTerminateFileLog function releases resources associated with a file log.
helpviewer_keywords: ["SetupTerminateFileLog","SetupTerminateFileLog function [Setup API]","_setupapi_setupterminatefilelog","setup.setupterminatefilelog","setupapi/SetupTerminateFileLog"]
old-location: setup\setupterminatefilelog.htm
tech.root: setup
ms.assetid: a230063a-2b4a-4ed3-8624-4859a17f8ccc
ms.date: 12/05/2018
ms.keywords: SetupTerminateFileLog, SetupTerminateFileLog function [Setup API], _setupapi_setupterminatefilelog, setup.setupterminatefilelog, setupapi/SetupTerminateFileLog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupTerminateFileLog
 - setupapi/SetupTerminateFileLog
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
 - SetupTerminateFileLog
---

# SetupTerminateFileLog function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupTerminateFileLog</b> function releases resources associated with a file log.

## -parameters

### -param FileLogHandle [in]

Handle to the log file as returned by a call to 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitializefileloga">SetupInitializeFileLog</a>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitializefileloga">SetupInitializeFileLog</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuplogfilea">SetupLogFile</a>