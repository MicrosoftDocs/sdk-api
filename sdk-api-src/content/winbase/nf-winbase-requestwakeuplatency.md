---
UID: NF:winbase.RequestWakeupLatency
title: RequestWakeupLatency function
author: windows-sdk-content
description: Has no effect and returns STATUS_NOT_SUPPORTED. This function is provided only for compatibility with earlier versions of Windows.Windows Server 2008 and Windows Vista:  Has no effect and always returns success.
old-location: base\requestwakeuplatency.htm
old-project: power
ms.assetid: f30fdfb6-dc7e-47fd-93ad-36655e65d0ae
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: LT_DONT_CARE, LT_LOWEST_LATENCY, RequestWakeupLatency, RequestWakeupLatency function, _win32_requestwakeuplatency, base.requestwakeuplatency, winbase/RequestWakeupLatency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - RequestWakeupLatency
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

