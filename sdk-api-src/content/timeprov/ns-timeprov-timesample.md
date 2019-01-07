---
UID: NS:timeprov.TimeSample
title: TimeSample
author: windows-sdk-content
description: Represents a time sample.
old-location: base\timesample_str.htm
tech.root: SysInfo
ms.assetid: 020a6502-3357-4800-8fc4-0d73ae42aa51
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSF_Authenticated, TSF_Hardware, TimeSample, TimeSample structure, _win32_timesample_str, base.timesample_str, timeprov/TimeSample
ms.topic: struct
req.header: timeprov.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - TimeSample
product: Windows
targetos: Windows
req.typenames: TimeSample
req.redist: 
---

# TimeSample structure


## -description


Represents a time sample.


## -struct-fields




### -field dwSize

The size of the structure, in bytes.


### -field dwRefid

A reference identifier for the time source, in NTP format (either an IP address or a four character ASCII string that describes the hardware source, such as GPS or WWVB).


### -field toOffset

The difference between local and remote clocks, in (10^-7)s.


### -field toDelay

The total roundtrip delay, in (10^-7)s. This is the time packets spent in transit from the root time source to the client, including root delay. For NTP providers, this means roundtrip delay to the peer, plus the peer's root delay. The hardware providers, this value is probably zero.


### -field tpDispersion

The total measurement error of the clock offset, including root dispersion, in (10^-7)s. This includes errors in reading the local clock, uncertainty in the local clock frequency, and error from filters. For NTP providers, this includes the peer's root dispersion.


### -field nSysTickCount

The value returned by 
<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfo</a> with TSI_TickCount.


### -field nSysPhaseOffset

The value returned by 
<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfo</a> with TSI_PhaseOffset.


### -field nLeapFlags

A variable that indicates an impending leap second or loss of synchronization. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Add leap second.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Subtract leap second.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Not synchronized.

</td>
</tr>
</table>
 


### -field nStratum

The number of network hops separating this computer from the root source. Hardware providers should return zero. NTP providers should return the stratum of the peer that provided the sample.


### -field dwTSFlags

The information about the time source. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TSF_Authenticated"></a><a id="tsf_authenticated"></a><a id="TSF_AUTHENTICATED"></a><dl>
<dt><b>TSF_Authenticated</b></dt>
</dl>
</td>
<td width="60%">
The sample has been cryptographically authenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="TSF_Hardware"></a><a id="tsf_hardware"></a><a id="TSF_HARDWARE"></a><dl>
<dt><b>TSF_Hardware</b></dt>
</dl>
</td>
<td width="60%">
The sample is from a hardware device such as a GPS or radio receiver.

</td>
</tr>
</table>
 


### -field wszUniqueName

The name that uniquely identifies the source of the sample. For network providers, the name should include the protocol and IP addresses. For hardware devices, the name should include the device name and communication port.


## -see-also




<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfoFunc</a>



<a href="https://msdn.microsoft.com/7e92a7c1-6927-4d53-8252-6bdd424d6e0c">TpcGetSamplesArgs</a>
 

 

