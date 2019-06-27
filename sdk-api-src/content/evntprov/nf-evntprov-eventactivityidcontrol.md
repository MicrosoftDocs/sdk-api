---
UID: NF:evntprov.EventActivityIdControl
title: EventActivityIdControl function (evntprov.h)
author: windows-sdk-content
description: Creates, queries, and sets the current activity identifier used by the EventWriteTransfer function.
old-location: etw\eventactivityidcontrol_func.htm
tech.root: ETW
ms.assetid: 1c412909-bdff-4181-9750-f3444fda4c8f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVENT_ACTIVITY_CTRL_CREATE_ID, EVENT_ACTIVITY_CTRL_CREATE_SET_ID, EVENT_ACTIVITY_CTRL_GET_ID, EVENT_ACTIVITY_CTRL_GET_SET_ID, EVENT_ACTIVITY_CTRL_SET_ID, EventActivityIdControl, EventActivityIdControl function [ETW], base.eventactivityidcontrol_func, etw.eventactivityidcontrol_func, evntprov/EventActivityIdControl
ms.topic: function
f1_keywords: 
 - "evntprov/EventActivityIdControl"
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
 - EventActivityIdControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventActivityIdControl function


## -description


Creates, queries, and sets the current activity identifier used by the 
   <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a> function.


## -parameters




### -param ControlCode [in]

A control code that specifies if you want to create, query or set the current activity identifier. You can specify one of the following codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_ACTIVITY_CTRL_GET_ID"></a><a id="event_activity_ctrl_get_id"></a><dl>
<dt><b>EVENT_ACTIVITY_CTRL_GET_ID</b></dt>
</dl>
</td>
<td width="60%">
Sets the <i>ActivityId</i> parameter to the current identifier value from thread local storage.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ACTIVITY_CTRL_SET_ID"></a><a id="event_activity_ctrl_set_id"></a><dl>
<dt><b>EVENT_ACTIVITY_CTRL_SET_ID</b></dt>
</dl>
</td>
<td width="60%">
Uses the identifier in the <i>ActivityId</i> parameter to set the value of the current identifier in the thread local storage.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ACTIVITY_CTRL_CREATE_ID"></a><a id="event_activity_ctrl_create_id"></a><dl>
<dt><b>EVENT_ACTIVITY_CTRL_CREATE_ID</b></dt>
</dl>
</td>
<td width="60%">
Creates a new identifier and sets the <i>ActivityId</i> parameter to the value of the new identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ACTIVITY_CTRL_GET_SET_ID"></a><a id="event_activity_ctrl_get_set_id"></a><dl>
<dt><b>EVENT_ACTIVITY_CTRL_GET_SET_ID</b></dt>
</dl>
</td>
<td width="60%">
Performs the following:

<ul>
<li>Copies the current identifier from thread local storage.</li>
<li>Sets the current identifier in thread local storage to the new identifier specified in the <i>ActivityId</i> parameter.</li>
<li>Sets the <i>ActivityId</i> parameter to the copy of the previous current identifier.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ACTIVITY_CTRL_CREATE_SET_ID"></a><a id="event_activity_ctrl_create_set_id"></a><dl>
<dt><b>EVENT_ACTIVITY_CTRL_CREATE_SET_ID</b></dt>
</dl>
</td>
<td width="60%">
Performs the following:

<ul>
<li>Copies the current identifier from thread local storage.</li>
<li>Creates a new identifier and sets the current identifier in thread local storage to the new identifier.</li>
<li>Sets the <i>ActivityId</i> parameter to the copy of the previous current identifier.</li>
</ul>
</td>
</tr>
</table>
 


### -param ActivityId [in, out]

A GUID that uniquely identifies the activity. To determine  when this parameter is an input parameter, an output parameter or both, see the descriptions for the <i>ControlCodes</i> parameter.


## -returns



Returns ERROR_SUCCESS if successful.




## -remarks



The EVENT_ACTIVITY_CTRL_GET_ID control code returns a GUID with all zeros (GUID_NULL) if the identifier has not been set.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>
 

 

