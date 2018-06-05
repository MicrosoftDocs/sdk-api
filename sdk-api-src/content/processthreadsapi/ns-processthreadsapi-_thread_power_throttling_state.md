---
UID: NS:processthreadsapi._THREAD_POWER_THROTTLING_STATE
title: "_THREAD_POWER_THROTTLING_STATE"
author: windows-sdk-content
description: Specifies the throttling policies and how to apply them to a target thread when that thread is subject to power management.
old-location: base\thread_power_throttling_state.htm
old-project: ProcThread
ms.assetid: 2E4D3A93-F4EE-4293-BE28-239B48E869B4
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: PTHREAD_POWER_THROTTLING_STATE, PTHREAD_POWER_THROTTLING_STATE structure pointer, THREAD_POWER_THROTTLING_CURRENT_VERSION, THREAD_POWER_THROTTLING_EXECUTION_SPEED, THREAD_POWER_THROTTLING_STATE, THREAD_POWER_THROTTLING_STATE structure, _THREAD_POWER_THROTTLING_STATE, base.thread_power_throttling_state, processthreadsapi/PTHREAD_POWER_THROTTLING_STATE, processthreadsapi/THREAD_POWER_THROTTLING_STATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: THREAD_POWER_THROTTLING_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processthreadsapi.h
api_name:
-	THREAD_POWER_THROTTLING_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

