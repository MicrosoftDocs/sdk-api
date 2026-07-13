---
UID: NF:setupapi.SetupLogFileW
title: SetupLogFileW function (setupapi.h)
description: The SetupLogFile function adds an entry to the log file. (Unicode)
helpviewer_keywords: ["SetupLogFile", "SetupLogFile function [Setup API]", "SetupLogFileW", "_setupapi_setuplogfile", "setup.setuplogfile", "setupapi/SetupLogFile", "setupapi/SetupLogFileW"]
old-location: setup\setuplogfile.htm
tech.root: setup
ms.assetid: bc738212-ff81-4b52-b2ef-50aabf6658ab
ms.date: 12/05/2018
ms.keywords: SetupLogFile, SetupLogFile function [Setup API], SetupLogFileA, SetupLogFileW, _setupapi_setuplogfile, setup.setuplogfile, setupapi/SetupLogFile, setupapi/SetupLogFileA, setupapi/SetupLogFileW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupLogFileW (Unicode) and SetupLogFileA (ANSI)
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
 - SetupLogFileW
 - setupapi/SetupLogFileW
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
 - SetupLogFile
 - SetupLogFileA
 - SetupLogFileW
---

# SetupLogFileW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupLogFile</b> function adds an entry to the log file.

## -parameters

### -param FileLogHandle [in]

Handle to the file log as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitializefileloga">SetupInitializeFileLog</a>. The caller must not have passed SPFILELOG_QUERYONLY when the log file was initialized.

### -param LogSectionName [in]

Optional pointer to the name for a logical grouping of names within the log file. You should use a <b>null</b>-terminated string.  Required if SPFILELOG_SYSTEMLOG was not passed when the file log was initialized. Otherwise, this parameter can be <b>NULL</b>.

### -param SourceFilename [in]

Name of the file as it exists on the source media from which it was installed. This name should be in whatever format is meaningful to the caller. You should use a <b>null</b>-terminated string.

### -param TargetFilename [in]

Name of the file as it exists on the target. This name should be in whatever format is meaningful to the caller. You should use a <b>null</b>-terminated string.

### -param Checksum [in]

Optional pointer to a  checksum value. Required for the system log.

### -param DiskTagfile [in]

Optional pointer to the tagfile for the media from which the file was installed. You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. Ignored for the system log if SPFILELOG_OEMFILE is not specified. Required for the system log if SPFILELOG_OEMFILE is specified. Otherwise, this parameter can be <b>NULL</b>.

### -param DiskDescription [in]

Optional pointer to the human-readable description of the media from which the file was installed. You should use a <b>null</b>-terminated string.  Ignored for the system log if SPFILELOG_OEMFILE is not specified in the <i>Flags</i> parameter.  Required for the system log if SPFILELOG_OEMFILE is specified in the Flags parameter. Otherwise, this parameter can be <b>NULL</b>.

### -param OtherInfo [in]

Optional pointer to additional information to be associated with the file. You should use a <b>null</b>-terminated string.  This parameter can be <b>NULL</b>.

### -param Flags [in]

This parameter can be SPFILELOG_OEMFILE, which is meaningful only for the system log and indicates that the file is not supplied by Microsoft. This parameter can be used to convert an existing file's entry, such as when an OEM overwrites a Microsoft-supplied system file.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovefilelogentrya">SetupRemoveFileLogEntry</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupLogFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
