---
UID: NF:winbase.RegisterEventSourceA
title: RegisterEventSourceA function (winbase.h)
description: Retrieves a registered handle to the specified event log. (ANSI)
helpviewer_keywords: ["RegisterEventSourceA", "winbase/RegisterEventSourceA"]
old-location: base\registereventsource.htm
tech.root: base
ms.assetid: 53706f83-6bc9-45d6-981c-bd0680d7bc08
ms.date: 12/05/2018
ms.keywords: RegisterEventSource, RegisterEventSource function, RegisterEventSourceA, RegisterEventSourceW, _win32_registereventsource, base.registereventsource, winbase/RegisterEventSource, winbase/RegisterEventSourceA, winbase/RegisterEventSourceW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterEventSourceA
 - winbase/RegisterEventSourceA
dev_langs:
 - c++
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
---

# RegisterEventSourceA function


## -description

Retrieves a registered handle to the specified event log.

## -parameters

### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which this operation is to be performed. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpSourceName [in]

The name of the <a href="/windows/desktop/EventLog/event-sources">event source</a> whose handle is to be retrieved. The source name must be a subkey of a log under the <b>Eventlog</b> registry key. 
						Note that the <b>Security</b> log is for system use only.

<div class="alert"><b>Note</b>  This string must not contain characters prohibited in XML Attributes, with the exception of XML Escape sequences such as <b>&amp;lt  &amp;gl</b>.</div>
<div> </div>

## -returns

If the function succeeds, the return value is a handle to the event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The function returns <b>ERROR_ACCESS_DENIED</b> if <i>lpSourceName</i> specifies the <b>Security</b> event log.

## -remarks

If the source name cannot be found, the event logging service uses the <b>Application</b> log. Although events will be reported , the events will not include descriptions because there are no message and category message files for looking up descriptions related to the event identifiers.

To close the handle to the event log, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-deregistereventsource">DeregisterEventSource</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/EventLog/reporting-an-event">Reporting an Event</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines RegisterEventSource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-deregistereventsource">DeregisterEventSource</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/EventLog/event-sources">Event Sources</a>



<a href="/windows/desktop/api/winbase/nf-winbase-reporteventa">ReportEvent</a>
