---
UID: NF:winbase.ClearEventLogA
title: ClearEventLogA function (winbase.h)
author: windows-sdk-content
description: Clears the specified event log, and optionally saves the current copy of the log to a backup file.
old-location: base\cleareventlog.htm
tech.root: EventLog
ms.assetid: b66896f6-baee-43c4-9d9b-5663c164d092
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClearEventLog, ClearEventLog function, ClearEventLogA, ClearEventLogW, _win32_cleareventlog, base.cleareventlog, winbase/ClearEventLog, winbase/ClearEventLogA, winbase/ClearEventLogW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClearEventLogA function


## -description


Clears the specified event log, and optionally saves the current copy of the log to a backup file.


## -parameters




### -param hEventLog [in]

A handle to the event log to be cleared. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> function returns this handle.


### -param lpBackupFileName [in]

The absolute or relative path of the backup file. If this file already exists, the function fails. 




If the <i>lpBackupFileName</i> parameter is <b>NULL</b>, the event log is not backed up.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The 
<b>ClearEventLog</b> function can fail if the event log is empty or the backup file already exists.




## -remarks



After this function returns, any handles that reference the cleared event log cannot be used to read the log.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>
 

 

