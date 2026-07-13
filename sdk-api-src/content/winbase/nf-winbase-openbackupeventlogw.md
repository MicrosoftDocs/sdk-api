---
UID: NF:winbase.OpenBackupEventLogW
title: OpenBackupEventLogW function (winbase.h)
description: Opens a handle to a backup event log created by the BackupEventLog function. (Unicode)
helpviewer_keywords: ["OpenBackupEventLog", "OpenBackupEventLog function", "OpenBackupEventLogW", "_win32_openbackupeventlog", "base.openbackupeventlog", "winbase/OpenBackupEventLog", "winbase/OpenBackupEventLogW"]
old-location: base\openbackupeventlog.htm
tech.root: base
ms.assetid: cfef0912-9d35-44aa-a1d3-f9bb37213ce0
ms.date: 12/05/2018
ms.keywords: OpenBackupEventLog, OpenBackupEventLog function, OpenBackupEventLogA, OpenBackupEventLogW, _win32_openbackupeventlog, base.openbackupeventlog, winbase/OpenBackupEventLog, winbase/OpenBackupEventLogA, winbase/OpenBackupEventLogW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenBackupEventLogW (Unicode) and OpenBackupEventLogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenBackupEventLogW
 - winbase/OpenBackupEventLogW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-eventlog-l1-1-2.dll
 - Advapi32.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
api_name:
 - OpenBackupEventLog
 - OpenBackupEventLogA
 - OpenBackupEventLogW
req.apiset: ext-ms-win-advapi32-eventlog-ansi-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# OpenBackupEventLogW function


## -description

Opens a handle to a backup event log created by the <a href="/windows/desktop/api/winbase/nf-winbase-backupeventloga">BackupEventLog</a> function.

## -parameters

### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which this operation is to be performed. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpFileName [in]

The full path of the backup file.

## -returns

If the function succeeds, the return value is a handle to the backup event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the backup filename specifies a remote server, the <i>lpUNCServerName</i> parameter must be <b>NULL</b>.

When this function is used on Windows Vista and later computers, only backup event logs that were saved with the <b>BackupEventLog</b> function on Windows Vista and later computers can be opened.





> [!NOTE]
> The winbase.h header defines OpenBackupEventLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-backupeventloga">BackupEventLog</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>
