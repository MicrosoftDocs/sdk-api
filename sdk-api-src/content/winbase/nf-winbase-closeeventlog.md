---
UID: NF:winbase.CloseEventLog
title: CloseEventLog function (winbase.h)
author: windows-sdk-content
description: Closes the specified event log.
old-location: base\closeeventlog.htm
tech.root: EventLog
ms.assetid: cb98a0cf-8ee9-4d78-8508-efae1d43a91d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseEventLog, CloseEventLog function, _win32_closeeventlog, base.closeeventlog, winbase/CloseEventLog
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - CloseEventLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseEventLog function


## -description


Closes the specified event log.


## -parameters




### -param hEventLog [in, out]

A handle to the event log to be closed. The 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a> function returns this handle.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>
 

 

