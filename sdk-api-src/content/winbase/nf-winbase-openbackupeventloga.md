---
UID: NF:winbase.OpenBackupEventLogA
title: OpenBackupEventLogA function
author: windows-sdk-content
description: Opens a handle to a backup event log created by the BackupEventLog function.
old-location: base\openbackupeventlog.htm
old-project: EventLog
ms.assetid: cfef0912-9d35-44aa-a1d3-f9bb37213ce0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: OpenBackupEventLog, OpenBackupEventLog function, OpenBackupEventLogA, OpenBackupEventLogW, _win32_openbackupeventlog, base.openbackupeventlog, winbase/OpenBackupEventLog, winbase/OpenBackupEventLogA, winbase/OpenBackupEventLogW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OpenBackupEventLogA function


## -description


Opens a handle to a backup event log created by the <a href="https://msdn.microsoft.com/5cfd5bad-4401-4abd-9e81-5f139e4ecf73">BackupEventLog</a> function.


## -parameters




### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which this operation is to be performed. If this parameter is <b>NULL</b>, the local computer is used.


### -param lpFileName [in]

The full path of the backup file.


## -returns



If the function succeeds, the return value is a handle to the backup event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the backup filename specifies a remote server, the <i>lpUNCServerName</i> parameter must be <b>NULL</b>.

When this function is used on Windows Vista and later computers, only backup event logs that were saved with the <b>BackupEventLog</b> function on Windows Vista and later computers can be opened.




## -see-also




<a href="https://msdn.microsoft.com/5cfd5bad-4401-4abd-9e81-5f139e4ecf73">BackupEventLog</a>



<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>
 

 

