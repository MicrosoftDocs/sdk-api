---
UID: NC:timeprov.GetTimeSysInfoFunc
title: GetTimeSysInfoFunc (timeprov.h)
description: Retrieves the system time state information.
helpviewer_keywords: ["GetTimeSysInfoFunc","GetTimeSysInfoFunc callback","GetTimeSysInfoFunc callback function","TSI_ClockPrecision","TSI_ClockTickSize","TSI_CurrentTime","TSI_LastSyncTime","TSI_LeapFlags","TSI_PhaseOffset","TSI_PollInterval","TSI_ReferenceIdentifier","TSI_RootDelay","TSI_RootDispersion","TSI_Stratum","TSI_TSFlags","TSI_TickCount","_win32_gettimesysinfo","base.gettimesysinfo","timeprov/GetTimeSysInfoFunc"]
old-location: base\gettimesysinfo.htm
tech.root: winprog
ms.assetid: e1b527e2-ab7c-4106-b203-e74b4ce2a89b
ms.date: 12/05/2018
ms.keywords: GetTimeSysInfoFunc, GetTimeSysInfoFunc callback, GetTimeSysInfoFunc callback function, TSI_ClockPrecision, TSI_ClockTickSize, TSI_CurrentTime, TSI_LastSyncTime, TSI_LeapFlags, TSI_PhaseOffset, TSI_PollInterval, TSI_ReferenceIdentifier, TSI_RootDelay, TSI_RootDispersion, TSI_Stratum, TSI_TSFlags, TSI_TickCount, _win32_gettimesysinfo, base.gettimesysinfo, timeprov/GetTimeSysInfoFunc
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTimeSysInfoFunc
 - timeprov/GetTimeSysInfoFunc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Timeprov.h
api_name:
 - GetTimeSysInfoFunc
---

# GetTimeSysInfoFunc callback function


## -description

Retrieves the system time state information.

## -parameters

### -param eInfo [in]

Requested state information. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TSI_ClockPrecision"></a><a id="tsi_clockprecision"></a><a id="TSI_CLOCKPRECISION"></a><dl>
<dt><b>TSI_ClockPrecision</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a signed <b>__int32</b> value that specifies the clock precision, in log2 seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_ClockTickSize"></a><a id="tsi_clockticksize"></a><a id="TSI_CLOCKTICKSIZE"></a><dl>
<dt><b>TSI_ClockTickSize</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is an unsigned <b>__int64</b> value that specifies the clock tick size, in (10^-7) seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_CurrentTime"></a><a id="tsi_currenttime"></a><a id="TSI_CURRENTTIME"></a><dl>
<dt><b>TSI_CurrentTime</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is an unsigned <b>__int64</b> value that specifies the current time, in (10^-7) second intervals that have elapsed since 12:00 A.M. January 1, 1601 Coordinated Universal Time (UTC).

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_LastSyncTime"></a><a id="tsi_lastsynctime"></a><a id="TSI_LASTSYNCTIME"></a><dl>
<dt><b>TSI_LastSyncTime</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is an unsigned <b>__int64</b> value that specifies the last synch time, in (10^-7) second intervals that have elapsed since 12:00 A.M. January 1, 1601 Coordinated Universal Time (UTC).

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_LeapFlags"></a><a id="tsi_leapflags"></a><a id="TSI_LEAPFLAGS"></a><dl>
<dt><b>TSI_LeapFlags</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a <b>BYTE</b> value that indicates an impending leap second or loss of synchronization. The following values are defined: 




<dl>
<dd>0 - No change</dd>
<dd>1 - Add leap second</dd>
<dd>2 - Subtract leap second</dd>
<dd>3 - Not synchronized</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="TSI_PhaseOffset"></a><a id="tsi_phaseoffset"></a><a id="TSI_PHASEOFFSET"></a><dl>
<dt><b>TSI_PhaseOffset</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a signed <b>__int64</b> value that specifies the phase offset used to adjust the clock, in seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_PollInterval"></a><a id="tsi_pollinterval"></a><a id="TSI_POLLINTERVAL"></a><dl>
<dt><b>TSI_PollInterval</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a signed <b>__int32</b> value that specifies the poll interval, in log2 seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_ReferenceIdentifier"></a><a id="tsi_referenceidentifier"></a><a id="TSI_REFERENCEIDENTIFIER"></a><dl>
<dt><b>TSI_ReferenceIdentifier</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a <b>DWORD</b> value that specifies the reference identifier for the time source, in NTP format (either an IP address or a four character ASCII string that describes the hardware source, such as Global Positioning System (GPS) or WWVB).

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_RootDelay"></a><a id="tsi_rootdelay"></a><a id="TSI_ROOTDELAY"></a><dl>
<dt><b>TSI_RootDelay</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a signed <b>__int64</b> value that specifies the root delay, in (10^-7) seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_RootDispersion"></a><a id="tsi_rootdispersion"></a><a id="TSI_ROOTDISPERSION"></a><dl>
<dt><b>TSI_RootDispersion</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is an unsigned <b>__int64</b> value that specifies, the root dispersion, in (10^-7) seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_Stratum"></a><a id="tsi_stratum"></a><a id="TSI_STRATUM"></a><dl>
<dt><b>TSI_Stratum</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a <b>BYTE</b> value that specifies the number of network hops that separate this computer from the root source. Hardware providers should return zero. NTP providers should return the stratum of the peer that provided the sample.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_TickCount"></a><a id="tsi_tickcount"></a><a id="TSI_TICKCOUNT"></a><dl>
<dt><b>TSI_TickCount</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is an unsigned <b>__int64</b> value that specifies the tick count (number of milliseconds since the system was started). This value will eventually wrap, so it should be used only to compare short intervals.

</td>
</tr>
<tr>
<td width="40%"><a id="TSI_TSFlags"></a><a id="tsi_tsflags"></a><a id="TSI_TSFLAGS"></a><dl>
<dt><b>TSI_TSFlags</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInfo</i> parameter is a <b>DWORD</b> value that specifies one of the following time source flags: 




<dl>
<dd>TSF_Authenticated</dd>
<dd>TSF_Hardware</dd>
<dd>TSF_IPv6</dd>
</dl>
</td>
</tr>
</table>

### -param pvInfo [out]

A pointer to a buffer that receives that state information. The format of this data depends on the value of <i>eInfo</i>.

## -returns

If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.

## -remarks

To ensure accuracy, the time provider should retrieve all time-related information using 
<b>GetTimeSysInfoFunc</b>. Note that the time values should not be used directly in an NTP packet. They are expressed relative to 12:00 A.M. January 1, 1601, whereas NTP specifies that time values be expressed relative to 12:00 A.M. January 1, 1900.

The 
<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a> function returns a pointer to this function.


#### Examples

For an example, see <a href="/windows/desktop/SysInfo/sample-time-provider">Sample Time Provider</a>.

<div class="code"></div>
