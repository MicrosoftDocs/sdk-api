---
UID: NF:fwpmu.FwpmEngineSetOption0
title: FwpmEngineSetOption0 function
author: windows-sdk-content
description: Changes the filter engine settings.
old-location: fwp\fwpmenginesetoption0.htm
old-project: fwp
ms.assetid: 6044a334-a1dc-4447-8581-cd0ffc5883db
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND, FWPM_ENGINE_OPTION_PACKET_QUEUE_NONE, FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND, FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST, FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST, FwpmEngineSetOption0, FwpmEngineSetOption0 function [Filtering], fwp.fwpmenginesetoption0, fwpmu/FwpmEngineSetOption0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmEngineSetOption0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmEngineSetOption0 function


## -description


The <b>FwpmEngineSetOption0</b> function changes the filter engine settings.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/e70986af-0c38-4fe6-a59f-3c45ce98bcc0">FWPM_ENGINE_OPTION</a></b>

The option to be set.


### -param newValue [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>*</b>

The new   option value. The data type contained in the <i>newValue</i> parameter should be  <b>FWP_UINT32</b>. 


When <i>option</i> is <b>FWPM_ENGINE_COLLECT_NET_EVENTS</b>, <i>newValue</i> should be one of the following.



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
Do not collect network events.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Collect network events. This is the default setting.

</td>
</tr>
</table>
 


When <i>option</i> is <b>FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS</b>, <i>newValue</i> should be either 0 (zero) or a bitwise combination of the following values.

<div class="alert"><b>Note</b>   If <i>newValue</i> is 0 the collection of inbound multicast and broadcast events is disabled. This is the default setting.</div>
<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST"></a><a id="fwpm_net_event_keyword_inbound_mcast"></a><dl>
<dt><b>FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Collect inbound multicast network events.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST"></a><a id="fwpm_net_event_keyword_inbound_bcast"></a><dl>
<dt><b>FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Collect inbound broadcast network events.

</td>
</tr>
</table>
 


When <i>option</i> is <b>FWPM_ENGINE_PACKET_QUEUING</b> (available only in Windows 8 and Windows Server 2012), <i>newValue</i> should be one of the following.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_ENGINE_OPTION_PACKET_QUEUE_NONE_"></a><a id="fwpm_engine_option_packet_queue_none_"></a><dl>
<dt><b>FWPM_ENGINE_OPTION_PACKET_QUEUE_NONE </b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not enable packet queuing.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND_"></a><a id="fwpm_engine_option_packet_queue_inbound_"></a><dl>
<dt><b>FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND </b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Enable inbound packet queuing.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND_"></a><a id="fwpm_engine_option_packet_queue_outbound_"></a><dl>
<dt><b>FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND </b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Enable outbound packet queuing.

</td>
</tr>
</table>
 


When <i>option</i> is <b>FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS</b> (available only in Windows 8 and Windows Server 2012), <i>newValue</i> should be the following. (<b>FwpmEngineSetOption0</b> may be used to enable connections, but will fail with <b>FWP_E_STILL_ON ERROR</b> when attempting to disable it.)



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The IPsec Connection Monitoring feature will be enabled.  New IPsec connection events will be logged as well as notifications sent.

</td>
</tr>
</table>
 


When <i>option</i> is <b>FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC</b>  (available only in Windows 8 and Windows Server 2012), <i>newValue</i> should be the time in milliseconds that specifies the maximum duration for a single WFP transaction.  Transactions taking longer than this duration will trigger a watchdog event.





The <b>FWPM_ENGINE_NAME_CACHE</b>  option is reserved for internal use.





## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The option was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

This function cannot be called from within a dynamic session. It will fail with
<b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about sessions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_WRITE</a> access to the filter engine. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

The default settings for network event collection are as follows:

<ul>
<li>Outbound, all (unicast, multicast, and broadcast) events  are collected.</li>
<li>Inbound, only unicast events are collected.</li>
</ul>
Network event collection settings persist across reboots.

To collect inbound broadcast and/or multicast network events,

<ol>
<li>Call <b>FwpmEngineSetOption0</b> with <i>option</i> set to FWPM_ENGINE_COLLECT_NET_EVENTS and <i>newValue</i> set to 1.</li>
<li> Call <b>FwpmEngineSetOption0</b> with <i>option</i> set to FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS and <i>newValue</i> parameter set to FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST and/or FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST.</li>
</ol>
To stop collecting inbound broadcast and/or multicast network events,

<ul>
<li> Call <b>FwpmEngineSetOption0</b> with <i>option</i> set to FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS and <i>newValue</i> parameter set to 0 (zero).</li>
</ul>
Disabling and re-enabling of network event collection (FWPM_ENGINE_COLLECT_NET_EVENTS) does not reset the collection of inbound broadcast and multicast events.

<b>FwpmEngineSetOption0</b> is a specific implementation of FwpmEngineSetOption. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e70986af-0c38-4fe6-a59f-3c45ce98bcc0">FWPM_ENGINE_OPTION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/e243f0d6-fb15-4c26-b41d-e33e96daf294">FwpmEngineGetOption0</a>
 

 

