---
UID: NS:processthreadsapi._PROCESS_LEAP_SECOND_INFO
title: PROCESS_LEAP_SECOND_INFO (processthreadsapi.h)
description: Specifies how the system handles positive leap seconds.
helpviewer_keywords: ["*PPROCESS_LEAP_SECOND_INFO","PPROCESS_LEAP_SECOND_INFO","PPROCESS_LEAP_SECOND_INFO structure pointer","PROCESS_LEAP_SECOND_INFO","PROCESS_LEAP_SECOND_INFO structure","PROCESS_LEAP_SECOND_INFO_FLAG_ENABLE_SIXTY_SECOND","base.process_leap_second_info","processthreadsapi/PPROCESS_LEAP_SECOND_INFO","processthreadsapi/PROCESS_LEAP_SECOND_INFO"]
old-location: base\process_leap_second_info.htm
tech.root: processthreadsapi
ms.assetid: 63AA6F71-506C-47EA-A7EF-8A8309B84257
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_LEAP_SECOND_INFO, PPROCESS_LEAP_SECOND_INFO, PPROCESS_LEAP_SECOND_INFO structure pointer, PROCESS_LEAP_SECOND_INFO, PROCESS_LEAP_SECOND_INFO structure, PROCESS_LEAP_SECOND_INFO_FLAG_ENABLE_SIXTY_SECOND, base.process_leap_second_info, processthreadsapi/PPROCESS_LEAP_SECOND_INFO, processthreadsapi/PROCESS_LEAP_SECOND_INFO'
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
req.typenames: PROCESS_LEAP_SECOND_INFO, *PPROCESS_LEAP_SECOND_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_LEAP_SECOND_INFO
 - processthreadsapi/_PROCESS_LEAP_SECOND_INFO
 - PPROCESS_LEAP_SECOND_INFO
 - processthreadsapi/PPROCESS_LEAP_SECOND_INFO
 - PROCESS_LEAP_SECOND_INFO
 - processthreadsapi/PROCESS_LEAP_SECOND_INFO
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
 - PROCESS_LEAP_SECOND_INFO
---

# PROCESS_LEAP_SECOND_INFO structure


## -description



Specifies how the system handles positive leap seconds.

## -struct-fields

### -field Flags

Currently, the only valid flag is <b>PROCESS_LEAP_SECOND_INFO_FLAG_ENABLE_SIXTY_SECOND</b>. That flag is described below.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESS_LEAP_SECOND_INFO_FLAG_ENABLE_SIXTY_SECOND"></a><a id="process_leap_second_info_flag_enable_sixty_second"></a><dl>
<dt><b>PROCESS_LEAP_SECOND_INFO_FLAG_ENABLE_SIXTY_SECOND</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
This value changes the way positive leap seconds are handled by system. Specifically, it changes how the seconds field during a positive leap second is handled by the system. If this value is used, then the positive leap second will be shown (For example: 23:59:59 -&gt; 23:59:60 -&gt; 00:00:00. If this value is not used, then "sixty seconds" is disabled, and the 59th second preceding a positive leap second will be shown for 2 seconds with the milliseconds value ticking twice as slow. So 23:59:59 -&gt; 23:59:59.500 -&gt; 00:00:00, which takes 2 seconds in wall clock time. Disabling "sixty second" can help with legacy apps that do not support seeing the seconds value as 60 during the positive leap second. Such apps may crash or misbehave. Therefore, in these cases, we display the 59th second for twice as long during the positive leap second. Note that this setting is per-process, and does not persist if the process is restarted. Developers should test their app for compatibility with seeing the system return "60", and add a call to their app startup routines to either enable or disable "sixty seconds". "Sixty seconds" is disabled by default for each process. Obviously, this setting has no effect if leap seconds are disabled system-wide, because then the system will never even encounter a leap second.

</td>
</tr>
</table>

### -field Reserved

Reserved for future use

