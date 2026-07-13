---
UID: NF:setupapi.SetupOpenLog
title: SetupOpenLog function (setupapi.h)
description: The SetupOpenLog function opens the log files.
helpviewer_keywords: ["SetupOpenLog","SetupOpenLog function [Setup API]","_setupapi_setupopenlog","setup.setupopenlog","setupapi/SetupOpenLog"]
old-location: setup\setupopenlog.htm
tech.root: setup
ms.assetid: 3ff13002-7811-4e44-b12b-52d0d4c8de60
ms.date: 12/05/2018
ms.keywords: SetupOpenLog, SetupOpenLog function [Setup API], _setupapi_setupopenlog, setup.setupopenlog, setupapi/SetupOpenLog
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
 - SetupOpenLog
 - setupapi/SetupOpenLog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-setupapi-logging-l1-1-0.dll
api_name:
 - SetupOpenLog
req.apiset: ext-ms-win-setupapi-logging-l1-1-0 (introduced in Windows 8)
---

# SetupOpenLog function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The  <b>SetupOpenLog</b> function opens the log files.

## -parameters

### -param Erase [in]

Must be FALSE.

## -returns

<b>TRUE</b> if the log file can be opened. <b>FALSE</b> if an error occurs. To get the  error code, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

 The log files are located in the Windows directory, and the file names are Setupact.log and Setuperr.log.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>
