---
UID: NF:timeprov.TimeProvCommand
title: TimeProvCommand function (timeprov.h)
description: A callback function that is called by the time provider manager to send commands to the time provider.
helpviewer_keywords: ["TPC_GetSamples","TPC_NetTopoChange","TPC_PollIntervalChanged","TPC_Query","TPC_Shutdown","TPC_TimeJumped","TPC_UpdateConfig","TimeProvCommand","TimeProvCommand callback","TimeProvCommand callback function","_win32_timeprovcommand","base.timeprovcommand","timeprov/TimeProvCommand"]
old-location: base\timeprovcommand.htm
tech.root: winprog
ms.assetid: 07b0bdf2-d224-4bbc-be29-9032a848d5ae
ms.date: 12/05/2018
ms.keywords: TPC_GetSamples, TPC_NetTopoChange, TPC_PollIntervalChanged, TPC_Query, TPC_Shutdown, TPC_TimeJumped, TPC_UpdateConfig, TimeProvCommand, TimeProvCommand callback, TimeProvCommand callback function, _win32_timeprovcommand, base.timeprovcommand, timeprov/TimeProvCommand
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
 - TimeProvCommand
 - timeprov/TimeProvCommand
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
 - TimeProvCommand
---

# TimeProvCommand function


## -description

A callback function that is called by the time provider manager to send commands to the time provider.

## -parameters

### -param hTimeProv [in]

A handle to the time provider. The 
<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a> function receives this handle.

### -param eCmd [in]

The command to be sent. This parameter can be one of the following values. 



<table>
<tr>
<th>Command</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPC_GetSamples"></a><a id="tpc_getsamples"></a><a id="TPC_GETSAMPLES"></a><dl>
<dt><b>TPC_GetSamples</b></dt>
</dl>
</td>
<td width="60%">
The time provider should return the time samples it has collected. If there is no data available, the provider should return no samples. For more details, see Remarks. 




The <i>pvArgs</i> parameter is pointer to a 
<a href="/windows/desktop/api/timeprov/ns-timeprov-tpcgetsamplesargs">TpcGetSamplesArgs</a> structure. The time provider manager provides the buffer for the samples. If the <i>pvArgs</i> buffer if too small, the provider should provide as many samples as is can and return ERROR_INSUFFICIENT_BUFFER. Any other error codes returned by the provider are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TPC_NetTopoChange"></a><a id="tpc_nettopochange"></a><a id="TPC_NETTOPOCHANGE"></a><dl>
<dt><b>TPC_NetTopoChange</b></dt>
</dl>
</td>
<td width="60%">
The network topology has changed. Network providers must redetect the network settings and verify that they can reach their sources. 




The <i>pvArgs</i> parameter indicates whether the change was requested by the user (NTC_UserRequested) or the system (NTC_Default).

</td>
</tr>
<tr>
<td width="40%"><a id="TPC_Query"></a><a id="tpc_query"></a><a id="TPC_QUERY"></a><dl>
<dt><b>TPC_Query</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="TPC_PollIntervalChanged"></a><a id="tpc_pollintervalchanged"></a><a id="TPC_POLLINTERVALCHANGED"></a><dl>
<dt><b>TPC_PollIntervalChanged</b></dt>
</dl>
</td>
<td width="60%">
The polling interval has changed. The time provider should call the 
<a href="/windows/desktop/api/timeprov/nc-timeprov-gettimesysinfofunc">GetTimeSysInfo</a> function to retrieve the new value. 




The <i>pvArgs</i> parameter is not used. Any error returned by the provider is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TPC_Shutdown"></a><a id="tpc_shutdown"></a><a id="TPC_SHUTDOWN"></a><dl>
<dt><b>TPC_Shutdown</b></dt>
</dl>
</td>
<td width="60%">
The system is shutting down. The time provider should exit within five seconds. 




The <i>pvArgs</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="TPC_TimeJumped"></a><a id="tpc_timejumped"></a><a id="TPC_TIMEJUMPED"></a><dl>
<dt><b>TPC_TimeJumped</b></dt>
</dl>
</td>
<td width="60%">
The system clock was adjusted abruptly, so the time provider should discard any time stamps it has saved. 




The <i>pvArgs</i> parameter indicates whether the time jump was requested by the user (TJF_UserRequested) or the system (TJF_Default).

</td>
</tr>
<tr>
<td width="40%"><a id="TPC_UpdateConfig"></a><a id="tpc_updateconfig"></a><a id="TPC_UPDATECONFIG"></a><dl>
<dt><b>TPC_UpdateConfig</b></dt>
</dl>
</td>
<td width="60%">
The time provider should verify whether its application-specific configuration data stored in the registry has changed. 




The <i>pvArgs</i> parameter is not used. Any error returned by the provider is ignored.

</td>
</tr>
</table>

### -param pvArgs [in]

A pointer to a buffer that specifies command information. The format of this data depends on the value of <i>eCmd</i>.

## -returns

If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.

## -remarks

The time provider should never take longer than half a second to return from this call.

When processing the TPC_GetSamples command, the provider should return one sample for each source it is monitoring. Therefore, a hardware provider should return one sample, while a network provider like NTP can return multiple samples. The provider should not return multiple samples from a single source; it should return the best sample from its cache of samples for the source. The provider can return the same sample on subsequent calls, provided that the data has not changed.


#### Examples

For an example, see <a href="/windows/desktop/SysInfo/sample-time-provider">Sample Time Provider</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/timeprov/nc-timeprov-gettimesysinfofunc">GetTimeSysInfoFunc</a>



<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a>



<a href="/windows/desktop/api/timeprov/ns-timeprov-tpcgetsamplesargs">TpcGetSamplesArgs</a>