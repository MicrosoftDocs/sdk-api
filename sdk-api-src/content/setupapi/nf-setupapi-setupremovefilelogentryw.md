---
UID: NF:setupapi.SetupRemoveFileLogEntryW
title: SetupRemoveFileLogEntryW function (setupapi.h)
description: The SetupRemoveFileLogEntry function removes an entry or section from a file log. (Unicode)
helpviewer_keywords: ["SetupRemoveFileLogEntry", "SetupRemoveFileLogEntry function [Setup API]", "SetupRemoveFileLogEntryW", "_setupapi_setupremovefilelogentry", "setup.setupremovefilelogentry", "setupapi/SetupRemoveFileLogEntry", "setupapi/SetupRemoveFileLogEntryW"]
old-location: setup\setupremovefilelogentry.htm
tech.root: setup
ms.assetid: a26d2c24-7092-40b0-9ae9-e7edf68aeb3d
ms.date: 12/05/2018
ms.keywords: SetupRemoveFileLogEntry, SetupRemoveFileLogEntry function [Setup API], SetupRemoveFileLogEntryA, SetupRemoveFileLogEntryW, _setupapi_setupremovefilelogentry, setup.setupremovefilelogentry, setupapi/SetupRemoveFileLogEntry, setupapi/SetupRemoveFileLogEntryA, setupapi/SetupRemoveFileLogEntryW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRemoveFileLogEntryW (Unicode) and SetupRemoveFileLogEntryA (ANSI)
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
 - SetupRemoveFileLogEntryW
 - setupapi/SetupRemoveFileLogEntryW
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
 - SetupRemoveFileLogEntry
 - SetupRemoveFileLogEntryA
 - SetupRemoveFileLogEntryW
---

# SetupRemoveFileLogEntryW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveFileLogEntry</b> function removes an entry or section from a file log.

## -parameters

### -param FileLogHandle [in]

Handle to the file log as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitializefileloga">SetupInitializeFileLog</a>. The caller must not have passed SPFILELOG_QUERYONLY when the log file was initialized.

### -param LogSectionName [in]

Pointer to a <b>null</b>-terminated string that specifies the name for a logical grouping of names within the log file. Required for non-system logs. Otherwise, <i>LogSectionName</i> may be <b>NULL</b>.

### -param TargetFilename [in]

Pointer to a <b>null</b>-terminated string that specifies the name of the file as it exists on the target. This name should be in whatever format is meaningful to the caller. If <b>NULL</b>, the section specified by <i>LogSectionName</i> is removed. The main section cannot be removed.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuplogfilea">SetupLogFile</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupRemoveFileLogEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
