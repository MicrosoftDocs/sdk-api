---
UID: NF:fwpmu.FwpmEngineGetOption0
title: FwpmEngineGetOption0 function
author: windows-sdk-content
description: Retrieves a filter engine option.
old-location: fwp\fwpmenginegetoption0.htm
tech.root: FWP
ms.assetid: e243f0d6-fb15-4c26-b41d-e33e96daf294
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND, FWPM_ENGINE_OPTION_PACKET_QUEUE_NONE, FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND, FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST, FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST, FwpmEngineGetOption0, FwpmEngineGetOption0 function [Filtering], fwp.fwpmenginegetoption0, fwpmu/FwpmEngineGetOption0
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmEngineGetOption0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmEngineGetOption0 function


## -description


The <b>FwpmEngineGetOption0</b> function retrieves a filter engine option.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/e70986af-0c38-4fe6-a59f-3c45ce98bcc0">FWPM_ENGINE_OPTION</a></b>

The option to be retrieved.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a>**</b>

The option value. The data    type contained in the <i>value</i> parameter will be <b>FWP_UINT32</b>.


If <i>option</i> is <b>FWPM_ENGINE_COLLECT_NET_EVENTS</b>, <i>value</i> will be one of the following.



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
Network events are not being collected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Network events are being collected.

</td>
</tr>
</table>
 


If <i>option</i> is <b>FWPM_ENGINE_NET_EVENT_MATCH_ANY_KEYWORDS</b>, <i>value</i> will be a bitwise combination of the following values.



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
Inbound multicast network events are being collected.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST"></a><a id="fwpm_net_event_keyword_inbound_bcast"></a><dl>
<dt><b>FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Inbound broadcast network events are not being collected.

</td>
</tr>
</table>
 


If <i>option</i> is <b>FWPM_ENGINE_PACKET_QUEUING</b> (available only in Windows 8 and Windows Server 2012),  <i>value</i> will be one of the following.



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
No packet queuing is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND_"></a><a id="fwpm_engine_option_packet_queue_inbound_"></a><dl>
<dt><b>FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND </b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Inbound packet queuing is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND_"></a><a id="fwpm_engine_option_packet_queue_outbound_"></a><dl>
<dt><b>FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND </b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Outbound packet queuing is enabled.

</td>
</tr>
</table>
 


If <i>option</i> is <b>FWPM_ENGINE_MONITOR_IPSEC_CONNECTIONS</b> (available only in Windows 8 and Windows Server 2012), <i>value</i> will be one of the following. 



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
The IPsec Connection Monitoring feature is disabled.  No IPsec connection events or notifications are being  logged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The IPsec Connection Monitoring feature is enabled.  New IPsec connection events and notifications are being logged.

</td>
</tr>
</table>
 


If <i>option</i> is <b>FWPM_ENGINE_TXN_WATCHDOG_TIMEOUT_IN_MSEC</b>  (available only in Windows 8 and Windows Server 2012), <i>value</i> will be the time in milliseconds that specifies the maximum duration for a single WFP transaction.  Transactions taking longer than this duration will trigger a watchdog event.




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
The option was retrieved successfully.

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



The caller must free the returned object by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the filter engine. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmEngineGetOption0</b> is a specific implementation of FwpmEngineGetOption. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example illustrates the use of <b>FwpmEngineGetOption0</b> to determine if network events are being collected.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;fwpmu.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "Fwpuclnt.lib")

void main()
{
    HANDLE engineHandle = NULL; 
    DWORD  result = ERROR_SUCCESS; 

    FWPM_ENGINE_OPTION option = FWPM_ENGINE_COLLECT_NET_EVENTS;
    FWP_VALUE0* fwpValue = NULL;

    result = FwpmEngineOpen0( NULL, RPC_C_AUTHN_WINNT, NULL, NULL, &amp;engineHandle );
    if (result != ERROR_SUCCESS)
    {
        printf("FwpmEngineOpen0 failed.\n");
        return;
    }

    result = FwpmEngineGetOption0( engineHandle, option, &amp;fwpValue);

    if (result != ERROR_SUCCESS)
    {
        printf("FwpmEngineGetOption0 failed.\n");
        return;
    }
    else if(fwpValue-&gt;type == FWP_UINT32)
    {
        if(fwpValue-&gt;uint32 == 1 ) 
            printf("Network events are being collected.\n");
        else
            printf("Network events are NOT being collected.\n");
    }
    else
        printf("Unexpected data type received.\n");

    FwpmFreeMemory0((void**)&amp;fwpValue); 

    return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e70986af-0c38-4fe6-a59f-3c45ce98bcc0">FWPM_ENGINE_OPTION</a>



<a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/6044a334-a1dc-4447-8581-cd0ffc5883db">FwpmEngineSetOption0</a>
 

 

