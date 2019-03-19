---
UID: NC:evntrace.WMIDPREQUEST
title: WMIDPREQUEST (evntrace.h)
author: windows-sdk-content
description: Providers implement this function to receive enable or disable notification requests from controllers. The WMIDPREQUEST type defines a pointer to this callback function. ControlCallback is a placeholder for the application-defined function name.
old-location: etw\controlcallback.htm
tech.root: ETW
ms.assetid: e9f70ae6-906f-4e55-bca7-4355f1ca6091
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ControlCallback, ControlCallback callback function [ETW], WMIDPREQUEST, WMIDPREQUEST callback, WMI_DISABLE_EVENTS, WMI_ENABLE_EVENTS, _evt_controlcallback, base.controlcallback, etw.controlcallback, evntrace/ControlCallback
ms.topic: callback
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Evntrace.h
api_name:
 - ControlCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WMIDPREQUEST callback function


## -description


Providers implement this function to receive enable or disable notification requests from controllers. 
			

The <b>WMIDPREQUEST</b> type defines a pointer to this callback function. <b>ControlCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param RequestCode [in]

Request code. Specify one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WMI_ENABLE_EVENTS"></a><a id="wmi_enable_events"></a><dl>
<dt><b>WMI_ENABLE_EVENTS</b></dt>
</dl>
</td>
<td width="60%">
Enables the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="WMI_DISABLE_EVENTS"></a><a id="wmi_disable_events"></a><dl>
<dt><b>WMI_DISABLE_EVENTS</b></dt>
</dl>
</td>
<td width="60%">
Disables the provider.

</td>
</tr>
</table>
 


### -param RequestContext


### -param *BufferSize


### -param Buffer [in]

Pointer to a 
<a href="https://msdn.microsoft.com/862a8f46-a326-48c6-92b7-8bb667837bb7">WNODE_HEADER</a> structure that contains information about the event tracing session for which the provider is being enabled or disabled.


#### - Context [in]

Provider-defined context. The provider uses the <i>RequestContext</i> parameter of  
<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> to specify the context.


#### - Reserved [in]

Reserved for internal use.


## -returns



You should return ERROR_SUCCESS if the callback succeeds. Note that ETW ignores the return value for this function except when a controller calls <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> to enable a provider and the provider has not yet called <a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a>. When this occurs, <b>RegisterTraceGuids</b> will return the return value of this callback if the registration was successful.
					




## -remarks



This function is specified using the 
<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function. When the controller calls the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function to enable, disable, or change the enable flags or level, ETW calls this callback. The provider enables or disables itself based the <i>RequestCode</i> value. Typically, the provider uses this value to set a global flag to indicate its enabled state.

The provider defines its interpretation of being enabled or disabled. Generally, if a provider is enabled, it generates events, but while it is disabled, it does not. 

ETW does not pass the enable flags and enable level that the controller passes to the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function to this callback. To retrieve this information, call the <a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a> and 
<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a> functions, respectively.

You also need to retrieve the session handle in this callback for future calls. To retrieve the session handle, call the <a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a> function.

Your callback function must not call anything that may incur LoadLibrary (more specifically, anything that requires a loader lock). 


#### Examples

For an example implementation of a 
<b>ControlCallback</b> function, see 
<a href="https://msdn.microsoft.com/21f62b5d-0a2d-468c-af88-2fab1512f0ec">Writing Classic Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>



<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a>



<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a>



<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a>



<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a>



<a href="https://msdn.microsoft.com/862a8f46-a326-48c6-92b7-8bb667837bb7">WNODE_HEADER</a>
 

 

