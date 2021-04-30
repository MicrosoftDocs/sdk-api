---
UID: NF:evntprov.EventProviderEnabled
title: EventProviderEnabled function (evntprov.h)
description: Determines if the event is enabled for any session.
helpviewer_keywords: ["EventProviderEnabled","EventProviderEnabled function [ETW]","WINEVENT_LEVEL_CRITICAL","WINEVENT_LEVEL_ERROR","WINEVENT_LEVEL_INFO","WINEVENT_LEVEL_VERBOSE","WINEVENT_LEVEL_WARNING","base.eventproviderenabled_func","etw.eventproviderenabled_func","evntprov/EventProviderEnabled"]
old-location: etw\eventproviderenabled_func.htm
tech.root: ETW
ms.assetid: 84c035b1-cdc7-47b7-b887-e5b508f17266
ms.date: 12/05/2018
ms.keywords: EventProviderEnabled, EventProviderEnabled function [ETW], WINEVENT_LEVEL_CRITICAL, WINEVENT_LEVEL_ERROR, WINEVENT_LEVEL_INFO, WINEVENT_LEVEL_VERBOSE, WINEVENT_LEVEL_WARNING, base.eventproviderenabled_func, etw.eventproviderenabled_func, evntprov/EventProviderEnabled
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventProviderEnabled
 - evntprov/EventProviderEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
 - EventProviderEnabled
---

# EventProviderEnabled function


## -description

Determines if the event is enabled for any session.

## -parameters

### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>.

### -param Level [in]

Level of detail included in the event. Specify one of the following levels that are defined in Winmeta.h. 
      Higher numbers imply that you get lower levels as well. For example, if you specify TRACE_LEVEL_WARNING, you 
      also receive all warning, error, and fatal events.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_LEVEL_CRITICAL"></a><a id="winevent_level_critical"></a><dl>
<dt><b>WINEVENT_LEVEL_CRITICAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Abnormal exit or termination events.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_LEVEL_ERROR"></a><a id="winevent_level_error"></a><dl>
<dt><b>WINEVENT_LEVEL_ERROR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Severe error events.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_LEVEL_WARNING"></a><a id="winevent_level_warning"></a><dl>
<dt><b>WINEVENT_LEVEL_WARNING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Warning events such as allocation failures.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_LEVEL_INFO"></a><a id="winevent_level_info"></a><dl>
<dt><b>WINEVENT_LEVEL_INFO</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Non-error events such as entry or exit events.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_LEVEL_VERBOSE"></a><a id="winevent_level_verbose"></a><dl>
<dt><b>WINEVENT_LEVEL_VERBOSE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Detailed trace events.

</td>
</tr>
</table>

### -param Keyword [in]

Bitmask that specifies the event category. This mask should be the same keyword mask that you defined in 
      the manifest for the event.

## -returns

Returns <b>TRUE</b> if the event is enabled for a session; otherwise, returns 
      <b>FALSE</b>.

## -remarks

Typically, providers do not call this function to determine if a session is expecting this event; they simply 
    write the event and ETW determines if the event is logged to the session.

Providers may want to call this function if they need to perform extra work to generate the event. In this 
    case, calling this function first (to determine if a session is expecting this event or not) may save resources 
    and time. 

The provider would call this function if the provider did not generate an 
    <a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structure for the event from the 
    manifest. If the event descriptor is available, call the 
    <a href="/windows/desktop/api/evntprov/nf-evntprov-eventenabled">EventEnabled</a> function.

## -see-also

<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventenabled">EventEnabled</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>