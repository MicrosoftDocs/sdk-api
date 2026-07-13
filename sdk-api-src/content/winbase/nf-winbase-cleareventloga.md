---
UID: NF:winbase.ClearEventLogA
title: ClearEventLogA function (winbase.h)
description: Clears the specified event log, and optionally saves the current copy of the log to a backup file. (ANSI)
helpviewer_keywords: ["ClearEventLogA", "winbase/ClearEventLogA"]
old-location: base\cleareventlog.htm
tech.root: base
ms.assetid: b66896f6-baee-43c4-9d9b-5663c164d092
ms.date: 12/05/2018
ms.keywords: ClearEventLog, ClearEventLog function, ClearEventLogA, ClearEventLogW, _win32_cleareventlog, base.cleareventlog, winbase/ClearEventLog, winbase/ClearEventLogA, winbase/ClearEventLogW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ClearEventLogW (Unicode) and ClearEventLogA (ANSI)
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
 - ClearEventLogA
 - winbase/ClearEventLogA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
api_name:
 - ClearEventLog
 - ClearEventLogA
 - ClearEventLogW
req.apiset: ext-ms-win-advapi32-eventlog-ansi-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# ClearEventLogA function


## -description

Clears the specified event log, and optionally saves the current copy of the log to a backup file.

## -parameters

### -param hEventLog [in]

A handle to the event log to be cleared. The <a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> function returns this handle.

### -param lpBackupFileName [in]

The absolute or relative path of the backup file. If this file already exists, the function fails. 




If the <i>lpBackupFileName</i> parameter is <b>NULL</b>, the event log is not backed up.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The 
<b>ClearEventLog</b> function can fail if the event log is empty or the backup file already exists.

## -remarks

After this function returns, any handles that reference the cleared event log cannot be used to read the log.





> [!NOTE]
> The winbase.h header defines ClearEventLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>
