---
UID: NF:winbase.OpenBackupEventLogW
title: OpenBackupEventLogW function (winbase.h)
author: windows-sdk-content
description: Opens a handle to a backup event log created by the BackupEventLog function.
old-location: base\openbackupeventlog.htm
tech.root: EventLog
ms.assetid: cfef0912-9d35-44aa-a1d3-f9bb37213ce0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenBackupEventLog, OpenBackupEventLog function, OpenBackupEventLogA, OpenBackupEventLogW, _win32_openbackupeventlog, base.openbackupeventlog, winbase/OpenBackupEventLog, winbase/OpenBackupEventLogA, winbase/OpenBackupEventLogW
ms.topic: function
f1_keywords: ["winbase/OpenBackupEventLog"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
api_name:
 - OpenBackupEventLog
 - OpenBackupEventLogA
 - OpenBackupEventLogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenBackupEventLogW function


## -description


Opens a handle to a backup event log created by the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-backupeventloga">BackupEventLog</a> function.


## -parameters




### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which this operation is to be performed. If this parameter is <b>NULL</b>, the local computer is used.


### -param lpFileName [in]

The full path of the backup file.


## -returns



If the function succeeds, the return value is a handle to the backup event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If the backup filename specifies a remote server, the <i>lpUNCServerName</i> parameter must be <b>NULL</b>.

When this function is used on Windows Vista and later computers, only backup event logs that were saved with the <b>BackupEventLog</b> function on Windows Vista and later computers can be opened.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-backupeventloga">BackupEventLog</a>



<a href="https://docs.microsoft.com/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>
 

 

