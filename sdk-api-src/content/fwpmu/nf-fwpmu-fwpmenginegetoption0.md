---
UID: NF:fwpmu.FwpmEngineGetOption0
title: FwpmEngineGetOption0 function (fwpmu.h)
description: Retrieves a filter engine option.
helpviewer_keywords: ["FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND","FWPM_ENGINE_OPTION_PACKET_QUEUE_NONE","FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND","FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST","FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST","FwpmEngineGetOption0","FwpmEngineGetOption0 function [Filtering]","fwp.fwpmenginegetoption0","fwpmu/FwpmEngineGetOption0"]
old-location: fwp\fwpmenginegetoption0.htm
tech.root: fwp
ms.assetid: e243f0d6-fb15-4c26-b41d-e33e96daf294
ms.date: 12/05/2018
ms.keywords: FWPM_ENGINE_OPTION_PACKET_QUEUE_INBOUND, FWPM_ENGINE_OPTION_PACKET_QUEUE_NONE, FWPM_ENGINE_OPTION_PACKET_QUEUE_OUTBOUND, FWPM_NET_EVENT_KEYWORD_INBOUND_BCAST, FWPM_NET_EVENT_KEYWORD_INBOUND_MCAST, FwpmEngineGetOption0, FwpmEngineGetOption0 function [Filtering], fwp.fwpmenginegetoption0, fwpmu/FwpmEngineGetOption0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmEngineGetOption0
 - fwpmu/FwpmEngineGetOption0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmEngineGetOption0
---

# FwpmEngineGetOption0 function


## -description

The <b>FwpmEngineGetOption0</b> function retrieves a filter engine option.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param option [in]

Type: [FWPM_ENGINE_OPTION](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_engine_option)</b>

The option to be retrieved.

### -param value [out]

Type: [FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)**</b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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

The caller must free the returned object by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the filter engine. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmEngineGetOption0</b> is a specific implementation of FwpmEngineGetOption. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example illustrates the use of <b>FwpmEngineGetOption0</b> to determine if network events are being collected.


```cpp
#include <windows.h>
#include <fwpmu.h>
#include <stdio.h>

#pragma comment(lib, "Fwpuclnt.lib")

void main()
{
    HANDLE engineHandle = NULL; 
    DWORD  result = ERROR_SUCCESS; 

    FWPM_ENGINE_OPTION option = FWPM_ENGINE_COLLECT_NET_EVENTS;
    FWP_VALUE0* fwpValue = NULL;

    result = FwpmEngineOpen0( NULL, RPC_C_AUTHN_WINNT, NULL, NULL, &engineHandle );
    if (result != ERROR_SUCCESS)
    {
        printf("FwpmEngineOpen0 failed.\n");
        return;
    }

    result = FwpmEngineGetOption0( engineHandle, option, &fwpValue);

    if (result != ERROR_SUCCESS)
    {
        printf("FwpmEngineGetOption0 failed.\n");
        return;
    }
    else if(fwpValue->type == FWP_UINT32)
    {
        if(fwpValue->uint32 == 1 ) 
            printf("Network events are being collected.\n");
        else
            printf("Network events are NOT being collected.\n");
    }
    else
        printf("Unexpected data type received.\n");

    FwpmFreeMemory0((void**)&fwpValue); 

    return;
}

```

## -see-also

[FWPM_ENGINE_OPTION](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_engine_option)



[FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmenginesetoption0">FwpmEngineSetOption0</a>