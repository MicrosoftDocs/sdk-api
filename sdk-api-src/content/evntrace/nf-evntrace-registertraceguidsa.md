---
UID: NF:evntrace.RegisterTraceGuidsA
title: RegisterTraceGuidsA function (evntrace.h)
author: windows-sdk-content
description: The RegisterTraceGuids function registers an event trace provider and the event trace classes that it uses to generate events. This function also specifies the function the provider uses to enable and disable tracing.
old-location: etw\registertraceguids.htm
tech.root: ETW
ms.assetid: c9158292-281b-4a02-b280-956e340d225c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RegisterTraceGuids, RegisterTraceGuids function [ETW], RegisterTraceGuidsA, RegisterTraceGuidsW, _evt_registertraceguids, base.registertraceguids, etw.registertraceguids, evntrace/RegisterTraceGuids, evntrace/RegisterTraceGuidsA, evntrace/RegisterTraceGuidsW
ms.topic: function
f1_keywords: 
 - "evntrace/RegisterTraceGuids"
dev_langs:
 - c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterTraceGuidsW (Unicode) and RegisterTraceGuidsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-eventing-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
 - RegisterTraceGuids
 - RegisterTraceGuidsA
 - RegisterTraceGuidsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegisterTraceGuidsA function


## -description


The 
<b>RegisterTraceGuids</b> function registers an event trace provider and the event trace classes that it uses to generate events. This function also specifies the function the provider uses  to enable and disable tracing. 
			
		


## -parameters




### -param RequestAddress [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> function that receives notification when the provider is enabled or disabled by an event tracing session. The <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> function calls the callback.


### -param RequestContext [in]

Pointer to an optional provider-defined context that ETW passes to the function specified by <i>RequestAddress</i>.


### -param ControlGuid [in]

 GUID of the registering provider.


### -param GuidCount [in]

Number of elements in the <i>TraceGuidReg</i> array.
					If <i>TraceGuidReg</i> is <b>NULL</b>, set this parameter to 0.


### -param TraceGuidReg [in, out]

Pointer to an array of  
<a href="https://docs.microsoft.com/windows/desktop/ETW/trace-guid-registration">TRACE_GUID_REGISTRATION</a> structures. 


Each element identifies a category of events that the provider provides. 

On input, the <b>Guid</b> member of each structure contains an event trace class GUID assigned by the registering provider. The class GUID identifies a category of events that the provider provides. Providers use the same class GUID to set the Guid member of <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> when calling the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceevent">TraceEvent</a> function to log the event. 

On output, the <b>RegHandle</b> member receives a handle to the event's class GUID registration. If the provider calls the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function, use the <b>RegHandle</b> member of <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-guid-registration">TRACE_GUID_REGISTRATION</a> to set the <b>RegHandle</b> member of <a href="https://docs.microsoft.com/windows/desktop/ETW/event-instance-header">EVENT_INSTANCE_HEADER</a>.

This parameter can be <b>NULL</b> if the provider calls only the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceevent">TraceEvent</a> function to log events. If the provider calls the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function to log events, this parameter cannot be <b>NULL</b>.


### -param MofImagePath [in]

 This parameter is not supported, set to <b>NULL</b>. You should use Mofcomp.exe to register the MOF resource during the setup of your application. For more information see, <a href="https://docs.microsoft.com/windows/desktop/ETW/publishing-your-event-schema">Publishing Your Event Schema</a>.

<b>Windows XP with SP1, Windows XP and Windows 2000:  </b>Pointer to an optional string that specifies the path of the DLL or executable program that contains the resource specified by <i>MofResourceName</i>. This parameter can be <b>NULL</b> if the event provider and consumer use another mechanism to share information about the event trace classes used by the provider. 





### -param MofResourceName [in]

 This parameter is not supported, set to <b>NULL</b>. You should use Mofcomp.exe to register the MOF resource during the setup of your application. For more information see, <a href="https://docs.microsoft.com/windows/desktop/ETW/publishing-your-event-schema">Publishing Your Event Schema</a>.

<b>Windows XP with SP1, Windows XP and Windows 2000:  </b>Pointer to an optional string that specifies the string resource of <i>MofImagePath</i>. The string resource contains the name of the binary MOF file that describes the event trace classes supported by the provider.


### -param RegistrationHandle [out]

Pointer to the provider's registration handle. Use this handle when you call the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/unregistertraceguids">UnregisterTraceGuids</a> function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.<div class="alert"><b>Note</b>  This function can return the return value from <a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> if a controller calls <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> to enable the provider and the provider has not yet called <b>RegisterTraceGuids</b>. When this occurs, <b>RegisterTraceGuids</b> will return the return value of the callback if the registration was successful.</div>
<div> </div>


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
<li><i>RequestAddress</i> is <b>NULL</b>.</li>
<li><i>ControlGuid</i> is <b>NULL</b>.</li>
<li><i>RegistrationHandle</i> is <b>NULL</b>.</li>
</ul>
<b>Windows XP and Windows 2000:  </b><i>TraceGuidReg</i> is <b>NULL</b> or <i>GuidCount</i> is less than or equal to zero.

</td>
</tr>
</table>
 




## -remarks



Providers call this function.

If the provider's <i>ControlGuid</i> has been previously registered and enabled, subsequent registrations that reference the same <i>ControlGuid</i> are automatically enabled.

 A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two. This limit includes those registered using this function and the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a> function.

<b>Prior to Windows Vista:  </b>There is no limit to the number of providers that a process can register.


#### Examples

For an example that uses 
<b>RegisterTraceGuids</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/ETW/tracing-events">Writing Classic Events</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/unregistertraceguids">UnregisterTraceGuids</a>
 

 

