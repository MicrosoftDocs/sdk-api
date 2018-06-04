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

# _THREAD_POWER_THROTTLING_STATE structure


## -description


Specifies the throttling policies and how to apply them to a target thread when that thread is subject to power management.


## -struct-fields




### -field Version

The version of the <b>THREAD_POWER_THROTTLING_STATE</b> structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="THREAD_POWER_THROTTLING_CURRENT_VERSION"></a><a id="thread_power_throttling_current_version"></a><dl>
<dt><b>THREAD_POWER_THROTTLING_CURRENT_VERSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The current version.

</td>
</tr>
</table>
 


### -field ControlMask

This field enables the caller to take control of the power throttling mechanism.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="THREAD_POWER_THROTTLING_EXECUTION_SPEED"></a><a id="thread_power_throttling_execution_speed"></a><dl>
<dt><b>THREAD_POWER_THROTTLING_EXECUTION_SPEED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Manages the execution speed of the thread.

</td>
</tr>
</table>
 


### -field StateMask

Manages the power throttling mechanism on/off state.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="THREAD_POWER_THROTTLING_EXECUTION_SPEED"></a><a id="thread_power_throttling_execution_speed"></a><dl>
<dt><b>THREAD_POWER_THROTTLING_EXECUTION_SPEED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Manages the execution speed of the thread.

</td>
</tr>
</table>
 

