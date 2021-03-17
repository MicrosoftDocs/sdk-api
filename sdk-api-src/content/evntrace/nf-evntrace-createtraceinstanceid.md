---
UID: NF:evntrace.CreateTraceInstanceId
title: CreateTraceInstanceId function (evntrace.h)
description: The CreateTraceInstanceId function creates a unique transaction identifier and maps it to a class GUID registration handle. You then use the transaction identifier when calling the TraceEventInstance function.
helpviewer_keywords: ["CreateTraceInstanceId","CreateTraceInstanceId function [ETW]","_evt_createtraceinstanceid","base.createtraceinstanceid","etw.createtraceinstanceid","evntrace/CreateTraceInstanceId"]
old-location: etw\createtraceinstanceid.htm
tech.root: ETW
ms.assetid: ab890392-f1e4-4b4e-a46c-8c7c2bfd3897
ms.date: 12/05/2018
ms.keywords: CreateTraceInstanceId, CreateTraceInstanceId function [ETW], _evt_createtraceinstanceid, base.createtraceinstanceid, etw.createtraceinstanceid, evntrace/CreateTraceInstanceId
req.header: evntrace.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateTraceInstanceId
 - evntrace/CreateTraceInstanceId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - CreateTraceInstanceId
---

# CreateTraceInstanceId function


## -description

The 
<b>CreateTraceInstanceId</b> function creates a unique transaction identifier and maps it to a class GUID registration handle. You then use the transaction identifier when calling the <a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function.

## -parameters

### -param RegHandle [in]

Handle to a registered event trace class. The 
<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function returns this handle in the <b>RegHandle</b> member of the <a href="/windows/desktop/ETW/trace-guid-registration">TRACE_GUID_REGISTRATION</a> structure.

### -param InstInfo [out]

Pointer to an 
<a href="/windows/desktop/ETW/event-instance-info">EVENT_INSTANCE_INFO</a> structure. The <b>InstanceId</b> member of this structure contains the transaction identifier.

## -returns

If the function is successful, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true:

<ul>
<li><i>RegHandle</i> is <b>NULL</b>.</li>
<li><i>pInstInfo</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
</table>

## -remarks

Providers call this function.

ETW creates the identifier in the user-mode process, thus it can return the same number for different processes. The value starts over at one when <b>InstanceId</b> reaches the maximum value for a <b>ULONG</b>. Only user-mode providers can call the <b>CreateTraceInstanceId</b> function; drivers cannot call this function. 


#### Examples

For an example that uses 
<b>CreateTraceInstanceId</b>, see 
<a href="/windows/desktop/ETW/tracing-event-instances">Tracing Event Instances</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a>



<a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a>