---
UID: NF:winbase.RegisterEventSourceA
title: RegisterEventSourceA function
author: windows-sdk-content
description: Retrieves a registered handle to the specified event log.
old-location: base\registereventsource.htm
tech.root: EventLog
ms.assetid: 53706f83-6bc9-45d6-981c-bd0680d7bc08
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegisterEventSource, RegisterEventSource function, RegisterEventSourceA, RegisterEventSourceW, _win32_registereventsource, base.registereventsource, winbase/RegisterEventSource, winbase/RegisterEventSourceA, winbase/RegisterEventSourceW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterEventSourceW (Unicode) and RegisterEventSourceA (ANSI)
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
 - API-MS-Win-EventLog-Legacy-l1-1-0.dll
 - advapi32legacy.dll
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - RegisterEventSource
 - RegisterEventSourceA
 - RegisterEventSourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterEventSourceA function


## -description


Retrieves a registered handle to the specified event log.


## -parameters




### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which this operation is to be performed. If this parameter is <b>NULL</b>, the local computer is used.


### -param lpSourceName [in]

The name of the <a href="https://msdn.microsoft.com/bc7fdc74-be41-4d17-997c-27171ef73f0f">event source</a> whose handle is to be retrieved. The source name must be a subkey of a log under the <b>Eventlog</b> registry key. 
						Note that the <b>Security</b> log is for system use only.

<div class="alert"><b>Note</b>  This string must not contain characters prohibited in XML Attributes, with the exception of XML Escape sequences such as <b>&amp;lt  &amp;gl</b>.</div>
<div> </div>

## -returns



If the function succeeds, the return value is a handle to the event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The function returns <b>ERROR_ACCESS_DENIED</b> if <i>lpSourceName</i> specifies the <b>Security</b> event log.




## -remarks



If the source name cannot be found, the event logging service uses the <b>Application</b> log. Although events will be reported , the events will not include descriptions because there are no message and category message files for looking up descriptions related to the event identifiers.

To close the handle to the event log, use the 
<a href="https://msdn.microsoft.com/f5d1f4b0-5320-4aec-a129-cafff6f1fed1">DeregisterEventSource</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/ace31e17-a638-414f-8518-9b944118047b">Reporting an Event</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f5d1f4b0-5320-4aec-a129-cafff6f1fed1">DeregisterEventSource</a>



<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/bc7fdc74-be41-4d17-997c-27171ef73f0f">Event Sources</a>



<a href="https://msdn.microsoft.com/e39273c3-9e42-41a1-9ec1-1cdff2ab7b55">ReportEvent</a>
 

 

