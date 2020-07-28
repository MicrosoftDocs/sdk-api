---
UID: NC:evntprov.PENABLECALLBACK
title: PENABLECALLBACK (evntprov.h)
description: Providers implement this function to receive enable or disable notification requests. The PENABLECALLBACK type defines a pointer to this callback function. EnableCallback is a placeholder for the application-defined function name.
helpviewer_keywords: ["EVENT_CONTROL_CODE_CAPTURE_STATE","EVENT_CONTROL_CODE_DISABLE_PROVIDER","EVENT_CONTROL_CODE_ENABLE_PROVIDER","PENABLECALLBACK","PENABLECALLBACK callback","PENABLECALLBACK callback function [ETW]","base.eanblecallback","etw.eanblecallback","etw.enablecallback","evntprov/PENABLECALLBACK"]
old-location: etw\enablecallback.htm
tech.root: ETW
ms.assetid: f339323e-9da9-495f-aac5-f44969a018eb
ms.date: 12/05/2018
ms.keywords: EVENT_CONTROL_CODE_CAPTURE_STATE, EVENT_CONTROL_CODE_DISABLE_PROVIDER, EVENT_CONTROL_CODE_ENABLE_PROVIDER, PENABLECALLBACK, PENABLECALLBACK callback, PENABLECALLBACK callback function [ETW], base.eanblecallback, etw.eanblecallback, etw.enablecallback, evntprov/PENABLECALLBACK
f1_keywords:
- evntprov/PENABLECALLBACK
dev_langs:
- c++
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Evntprov.h
api_name:
- PENABLECALLBACK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PENABLECALLBACK callback function


## -description


Providers implement this function to receive enable or disable notification requests. 
			

The <b>PENABLECALLBACK</b> type defines a pointer to this callback function. <b>EnableCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param SourceId [in]

GUID that identifies the session that enabled the provider. The value is GUID_NULL if <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> did not specify a source identifier.


### -param IsEnabled [in]

Indicates if the session is enabling or disabling the provider. A value of zero indicates that the session is disabling the provider. A value of 1 indicates that the session is enabling the provider. Beginning with Windows 7, this value can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_CONTROL_CODE_DISABLE_PROVIDER"></a><a id="event_control_code_disable_provider"></a><dl>
<dt><b>EVENT_CONTROL_CODE_DISABLE_PROVIDER</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The session is disabling the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_CONTROL_CODE_ENABLE_PROVIDER"></a><a id="event_control_code_enable_provider"></a><dl>
<dt><b>EVENT_CONTROL_CODE_ENABLE_PROVIDER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The session is enabling the provider. 

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_CONTROL_CODE_CAPTURE_STATE"></a><a id="event_control_code_capture_state"></a><dl>
<dt><b>EVENT_CONTROL_CODE_CAPTURE_STATE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The session is requesting that the provider log its state information. The provider determines the state information that it logs.

</td>
</tr>
</table>
 

If you receive a value (for example,  EVENT_CONTROL_CODE_CAPTURE_STATE) that you do not support, ignore the value (do not fail).


### -param Level [in]

Provider-defined value that specifies the verboseness of the events that the provider writes. The provider must write the event if this value is less than or equal to the level value that the event defines. 

This value is passed in the <i>Level</i> parameter of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> function or the <i>EnableLevel</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>.


### -param MatchAnyKeyword [in]

Bitmask of keywords that the provider uses to determine the category of events that it writes. 

This value is passed in the <i>MatchAnyKeyword</i> parameter of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> function or the <i>EnableFlag</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>.


### -param MatchAllKeyword


### -param FilterData [in, optional]

A list of filter data that one or more sessions passed to the provider. A session can specify only one filter but the list will contain filters from all sessions that used filter data to enable the provider.

The filter data is valid only within the callback, so providers should make a local copy of the data. 


### -param CallbackContext [in, optional]

Context of the callback defined when the provider called <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a> to register itself.


#### - MatchAllKeywords [in]

This bitmask is optional. This mask further restricts the category of  events that the provider writes. 

This value is passed in the <i>MatchAllKeywords</i> parameter of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> function.


## -remarks



To specify that you want to receive notification when a session enables or disables your provider, set the <i>EnableCallback</i> parameter when calling the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a> function.

<a href="https://docs.microsoft.com/windows/desktop/ETW/about-event-tracing">Classic</a> providers needed to specify and implement a callback because it used the information that was passed to the callback to determine the types of events to log and the level of verboseness to use when logging the events. However, with <a href="https://docs.microsoft.com/windows/desktop/ETW/about-event-tracing">manifest-based</a> providers, the callback is optional and is used for informational purposes; you do not need to specify or implement the callback when registering the provider unless your provider supports filtering. Providers can now just write events and ETW will determine if the event is logged to the session. If you want to verify that the event should be written before writing the event, you can call either the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventenabled">EventEnabled</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventproviderenabled">EventProviderEnabled</a> function.

Each time a new session enables the provider or a current session updates the provider, ETW calls the provider's callback function, if implemented. The level value that ETW passes to the callback is the highest level value specified amongst all the sessions. For example, if session A enabled the provider for warning (3) events and then session B enabled the provider for critical (1) events, the level value for the second callback is also 3, not 1.

The MatchAnyKeyword value that ETW passes to the callback is a composite value of all MatchAnyKeyword values specified for all sessions that enabled the provider. The same is true for the MatchAllKeywords value. The SourceId and FilterData values are those values passed to the <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> call.

Your callback function must not call anything that may incur LoadLibrary (more specifically, anything that requires a loader lock). 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>
 

 

