---
UID: NS:processthreadsapi._PROCESS_POWER_THROTTLING_STATE
title: PROCESS_POWER_THROTTLING_STATE (processthreadsapi.h)
description: Specifies the throttling policies and how to apply them to a target process when that process is subject to power management.
helpviewer_keywords: ["*PPROCESS_POWER_THROTTLING_STATE","PPROCESS_POWER_THROTTLING_STATE","PPROCESS_POWER_THROTTLING_STATE structure pointer","PROCESS_POWER_THROTTLING_CURRENT_VERSION","PROCESS_POWER_THROTTLING_EXECUTION_SPEED","PROCESS_POWER_THROTTLING_STATE","PROCESS_POWER_THROTTLING_STATE structure","base.process_power_throttling_state","processthreadsapi/PPROCESS_POWER_THROTTLING_STATE","processthreadsapi/PROCESS_POWER_THROTTLING_STATE"]
old-location: base\process_power_throttling_state.htm
tech.root: processthreadsapi
ms.assetid: 394B6509-849C-4B4C-9A46-AF5011A03585
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_POWER_THROTTLING_STATE, PPROCESS_POWER_THROTTLING_STATE, PPROCESS_POWER_THROTTLING_STATE structure pointer, PROCESS_POWER_THROTTLING_CURRENT_VERSION, PROCESS_POWER_THROTTLING_EXECUTION_SPEED, PROCESS_POWER_THROTTLING_STATE, PROCESS_POWER_THROTTLING_STATE structure, base.process_power_throttling_state, processthreadsapi/PPROCESS_POWER_THROTTLING_STATE, processthreadsapi/PROCESS_POWER_THROTTLING_STATE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROCESS_POWER_THROTTLING_STATE, *PPROCESS_POWER_THROTTLING_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_POWER_THROTTLING_STATE
 - processthreadsapi/_PROCESS_POWER_THROTTLING_STATE
 - PPROCESS_POWER_THROTTLING_STATE
 - processthreadsapi/PPROCESS_POWER_THROTTLING_STATE
 - PROCESS_POWER_THROTTLING_STATE
 - processthreadsapi/PROCESS_POWER_THROTTLING_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - PROCESS_POWER_THROTTLING_STATE
---

# PROCESS_POWER_THROTTLING_STATE structure


## -description

Specifies the throttling policies and how to apply them to a target process when that process is subject to power management. This structure is used by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetProcessInformation</a> function.

## -struct-fields

### -field Version

The version of the <b>PROCESS_POWER_THROTTLING_STATE</b> structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESS_POWER_THROTTLING_CURRENT_VERSION"></a><a id="process_power_throttling_current_version"></a><dl>
<dt><b>PROCESS_POWER_THROTTLING_CURRENT_VERSION</b></dt>
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
<td width="40%"><a id="PROCESS_POWER_THROTTLING_EXECUTION_SPEED"></a><a id="process_power_throttling_execution_speed"></a><dl>
<dt><b>PROCESS_POWER_THROTTLING_EXECUTION_SPEED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Manages the execution speed of the process.

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
<td width="40%"><a id="PROCESS_POWER_THROTTLING_EXECUTION_SPEED"></a><a id="process_power_throttling_execution_speed"></a><dl>
<dt><b>PROCESS_POWER_THROTTLING_EXECUTION_SPEED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Manages the execution speed of the process.

</td>
</tr>
</table>