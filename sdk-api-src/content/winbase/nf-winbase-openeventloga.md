---
UID: NF:winbase.OpenEventLogA
title: OpenEventLogA function
author: windows-sdk-content
description: Opens a handle to the specified event log.
old-location: base\openeventlog.htm
old-project: EventLog
ms.assetid: 6cd8797a-aeaf-4603-b43c-b1ff45b6200a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: OpenEventLog, OpenEventLog function, OpenEventLogA, OpenEventLogW, _win32_openeventlog, base.openeventlog, winbase/OpenEventLog, winbase/OpenEventLogA, winbase/OpenEventLogW
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
req.unicode-ansi: OpenEventLogW (Unicode) and OpenEventLogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
-	Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
-	Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
-	OpenEventLog
-	OpenEventLogA
-	OpenEventLogW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OpenEventLogA function


## -description


Opens a handle to the specified event log.


## -parameters




### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which the event log is to be opened. If this parameter is <b>NULL</b>, the local computer is used.


### -param lpSourceName [in]

The name of the log. 

If you specify a custom log and it cannot be found, the event logging service opens the <b>Application</b> log; however, there will be no associated message or category string file.


## -returns




						If the function succeeds, the return value is the handle to an event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To close the handle to the event log, use the 
<a href="https://msdn.microsoft.com/cb98a0cf-8ee9-4d78-8508-efae1d43a91d">CloseEventLog</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e03d2ab5-50ea-4916-9774-850506714538">Querying for Event Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b66896f6-baee-43c4-9d9b-5663c164d092">ClearEventLog</a>



<a href="https://msdn.microsoft.com/cb98a0cf-8ee9-4d78-8508-efae1d43a91d">CloseEventLog</a>



<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/87d860e3-2495-4e15-bb42-341e92935e55">Eventlog Key</a>



<a href="https://msdn.microsoft.com/10b37174-661a-4dc6-a7fe-752739494156">ReadEventLog</a>



<a href="https://msdn.microsoft.com/e39273c3-9e42-41a1-9ec1-1cdff2ab7b55">ReportEvent</a>
 

 

