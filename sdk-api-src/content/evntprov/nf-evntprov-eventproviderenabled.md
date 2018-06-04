---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EventProviderEnabled function


## -description


Determines if the event is enabled for any session.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>.


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
    <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure for the event from the 
    manifest. If the event descriptor is available, call the 
    <a href="https://msdn.microsoft.com/b332b6d4-6921-40bd-bebc-6646b5b9bcde">EventEnabled</a> function.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/b332b6d4-6921-40bd-bebc-6646b5b9bcde">EventEnabled</a>



<a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>
 

 

