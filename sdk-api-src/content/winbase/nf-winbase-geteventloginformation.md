---
UID: NF:winbase.GetEventLogInformation
title: GetEventLogInformation function
author: windows-sdk-content
description: Retrieves information about the specified event log.
old-location: base\geteventloginformation.htm
old-project: eventlog
ms.assetid: 627e0af2-3ce6-47fe-89c6-d7c0483cb94b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EVENTLOG_FULL_INFO, GetEventLogInformation, GetEventLogInformation function, _win32_geteventloginformation, base.geteventloginformation, winbase/GetEventLogInformation
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
req.unicode-ansi: 
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
 - API-MS-Win-EventLog-Legacy-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - GetEventLogInformation
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetEventLogInformation function


## -description


Retrieves information about the specified event log.


## -parameters




### -param hEventLog [in]

A handle to the event log. The 
<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a> or 
<a href="https://msdn.microsoft.com/53706f83-6bc9-45d6-981c-bd0680d7bc08">RegisterEventSource</a> function returns this handle.


### -param dwInfoLevel [in]

The level of event log information to return. 



					This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_FULL_INFO"></a><a id="eventlog_full_info"></a><dl>
<dt><b>EVENTLOG_FULL_INFO</b></dt>
</dl>
</td>
<td width="60%">
Indicate whether the specified log is full. The <i>lpBuffer</i> parameter will contain an 
<a href="https://msdn.microsoft.com/3ca41d6b-51a6-4226-89be-ab2c37628289">EVENTLOG_FULL_INFORMATION</a> structure.

</td>
</tr>
</table>
 


### -param lpBuffer [out]

An application-allocated buffer that receives the event log information. The format of this data depends on the value of the <i>dwInfoLevel</i> parameter.


### -param cbBufSize [in]

The size of the <i>lpBuffer</i> buffer, in bytes.


### -param pcbBytesNeeded [out]

The function sets this parameter to the required buffer size for the requested information, regardless of whether the function succeeds. Use this value if the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b> to allocate a buffer of the correct size.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ca41d6b-51a6-4226-89be-ab2c37628289">EVENTLOG_FULL_INFORMATION</a>



<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a>



<a href="https://msdn.microsoft.com/53706f83-6bc9-45d6-981c-bd0680d7bc08">RegisterEventSource</a>
 

 

