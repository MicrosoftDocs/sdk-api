---
UID: NF:evntrace.CreateTraceInstanceId
title: CreateTraceInstanceId function
author: windows-sdk-content
description: The CreateTraceInstanceId function creates a unique transaction identifier and maps it to a class GUID registration handle. You then use the transaction identifier when calling the TraceEventInstance function.
old-location: etw\createtraceinstanceid.htm
tech.root: etw
ms.assetid: ab890392-f1e4-4b4e-a46c-8c7c2bfd3897
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateTraceInstanceId, CreateTraceInstanceId function [ETW], _evt_createtraceinstanceid, base.createtraceinstanceid, etw.createtraceinstanceid, evntrace/CreateTraceInstanceId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - CreateTraceInstanceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateTraceInstanceId function


## -description


The 
<b>CreateTraceInstanceId</b> function creates a unique transaction identifier and maps it to a class GUID registration handle. You then use the transaction identifier when calling the <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> function.
		


## -parameters




### -param RegHandle [in]

Handle to a registered event trace class. The 
<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function returns this handle in the <b>RegHandle</b> member of the <a href="https://msdn.microsoft.com/fc7b61fb-ef1c-48ec-8523-5f3114b5407a">TRACE_GUID_REGISTRATION</a> structure.
					


### -param InstInfo

TBD




#### - pInstInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/83a3802c-b992-43a2-a98a-bdee2ecfef24">EVENT_INSTANCE_INFO</a> structure. The <b>InstanceId</b> member of this structure contains the transaction identifier.


## -returns



If the function is successful, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some common errors and their causes.

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
<a href="https://msdn.microsoft.com/246e9443-3120-49bf-a6e3-64dddba348fa">Tracing Event Instances</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a>



<a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a>
 

 

