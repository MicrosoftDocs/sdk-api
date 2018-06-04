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

# RequestWakeupLatency function


## -description


<p class="CCE_Message">[<b>RequestWakeupLatency</b> 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Has no effect and returns <b>STATUS_NOT_SUPPORTED</b>. This function is provided only for compatibility with earlier versions of Windows.

<b>Windows Server 2008 and Windows Vista:  </b>Has no effect and always returns success. 


## -parameters




### -param latency [in]

The latency requirement for the time is takes to wake the computer. This parameter can be one of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LT_LOWEST_LATENCY"></a><a id="lt_lowest_latency"></a><dl>
<dt><b>LT_LOWEST_LATENCY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
PowerSystemSleeping1 state (equivalent to ACPI state S0 and APM state Working).

</td>
</tr>
<tr>
<td width="40%"><a id="LT_DONT_CARE"></a><a id="lt_dont_care"></a><dl>
<dt><b>LT_DONT_CARE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Any latency (default).

</td>
</tr>
</table>
 


## -returns



The return value is nonzero.
      




## -remarks



The system uses the wake-up latency requirement when choosing a sleeping state. The latency is not guaranteed 
    because wake-up time is determined by the hardware design of the particular computer.

To cancel a latency request, call 
    <b>RequestWakeupLatency</b> with 
    <b>LT_DONT_CARE</b>.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

