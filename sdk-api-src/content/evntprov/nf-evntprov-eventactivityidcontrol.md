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

# EventActivityIdControl function


## -description


Creates, queries, and sets the current activity identifier used by the 
   <a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a> function.


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




<a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a>
 

 

