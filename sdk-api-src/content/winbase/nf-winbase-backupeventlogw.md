---
UID: NF:winbase.BackupEventLogW
title: BackupEventLogW function (winbase.h)
description: Saves the specified event log to a backup file.
helpviewer_keywords: ["BackupEventLog","BackupEventLog function","BackupEventLogA","BackupEventLogW","_win32_backupeventlog","base.backupeventlog","winbase/BackupEventLog","winbase/BackupEventLogA","winbase/BackupEventLogW"]
old-location: base\backupeventlog.htm
tech.root: base
ms.assetid: 5cfd5bad-4401-4abd-9e81-5f139e4ecf73
ms.date: 12/05/2018
ms.keywords: BackupEventLog, BackupEventLog function, BackupEventLogA, BackupEventLogW, _win32_backupeventlog, base.backupeventlog, winbase/BackupEventLog, winbase/BackupEventLogA, winbase/BackupEventLogW
f1_keywords:
- winbase/BackupEventLog
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BackupEventLogW (Unicode) and BackupEventLogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
api_name:
- BackupEventLog
- BackupEventLogA
- BackupEventLogW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BackupEventLogW function


## -description


Saves the specified event log to a backup file. The function does not clear the event log.


## -parameters




### -param hEventLog [in]

A handle to the open event log. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> function returns this handle.


### -param lpBackupFileName [in]

The absolute or relative path of the backup file.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>BackupEventLog</b> function fails with the ERROR_PRIVILEGE_NOT_HELD error if the user does not have the SE_BACKUP_NAME privilege.





> [!NOTE]
> The winbase.h header defines BackupEventLog as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>
 

 

