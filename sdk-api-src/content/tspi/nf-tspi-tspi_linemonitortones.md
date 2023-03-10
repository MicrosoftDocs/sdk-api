---
UID: NF:tspi.TSPI_lineMonitorTones
title: TSPI_lineMonitorTones function (tspi.h)
description: The TSPI_lineMonitorTones function enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the client application through TAPI.
helpviewer_keywords: ["TSPI_lineMonitorTones","TSPI_lineMonitorTones function [TAPI 2.2]","_tspi_tspi_linemonitortones","tspi.tspi_linemonitortones","tspi/TSPI_lineMonitorTones"]
old-location: tspi\tspi_linemonitortones.htm
tech.root: tapi3
ms.assetid: 8b16dda3-bcb4-4a89-b2e5-b9330be3eb01
ms.date: 12/05/2018
ms.keywords: TSPI_lineMonitorTones, TSPI_lineMonitorTones function [TAPI 2.2], _tspi_tspi_linemonitortones, tspi.tspi_linemonitortones, tspi/TSPI_lineMonitorTones
req.header: tspi.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineMonitorTones
 - tspi/TSPI_lineMonitorTones
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineMonitorTones
---

# TSPI_lineMonitorTones function


## -description

The 
<b>TSPI_lineMonitorTones</b> function enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the client application through TAPI.

## -parameters

### -param hdCall

The handle to the call for which tone detection is to be done. The call state of <i>hdCall</i> can be any state except <i>idle</i>.

### -param dwToneListID

The unique identifier for this tone list. Several tone lists can be outstanding at one time. The service provider must replace any old list having the same <i>dwToneListID</i> with the new tone list. If <i>lpToneList</i> is <b>NULL</b>, the tone list with <i>dwToneListID</i> is simply dropped. In any case, other tone lists with different <i>dwToneListID</i>s are kept unchanged.

### -param lpToneList

A list of tones to be monitored, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linemonitortone">LINEMONITORTONE</a>. Each tone in this list has an application-defined tag field that is used to identify individual tones in the list for the purpose of reporting a tone detection. Tone monitoring in progress is canceled or changed by calling this operation with either <b>NULL</b> for <i>lpToneList</i> or with another tone list. The service provider must copy the tone list into its own memory for later reference, rather than simply retaining the pointer into application memory.

### -param dwNumEntries

The number of entries in <i>lpToneList</i>. The <i>dwNumEntries</i> parameter is ignored if <i>lpToneList</i> is <b>NULL</b>. TAPI does not validate this parameter when this function is called.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALTONE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_INVALPOINTER.

## -remarks

This function returns zero (success) when tone monitoring is correctly initiated, not when tone monitoring is terminated. As with media monitoring, tone monitoring remains in effect for a given tone list until that tone list is explicitly disabled by calling 
<b>TSPI_lineMonitorTones</b> with the same <i>dwToneListID</i> and another tone list (or a <b>NULL</b> tone list), or until the call transitions to <i>idle</i>.

Although this function can be invoked in any call state except <i>idle</i>, tones can typically only be detected while the call is in the <i>connected</i> state. Tone detection usually requires computational resources. Depending on the service provider and other activities that compete for such resources, the number of tones that can be detected can vary over time. Also, an equivalent amount of resources can be consumed for monitoring a single triple frequency tone versus three single frequency tones. If resources are overcommitted, the service provider returns LINEERR_RESOURCEUNAVAIL.

The service provider monitors for all tones in all tone lists concurrently. When a tone is detected, each matching tone from each tone list is reported separately using a 
<a href="/previous-versions/windows/desktop/legacy/ms725234(v=vs.85)">LINE_MONITORTONE</a> message. Each tone report includes both the tone list identifier and the application-specific tag. Some service providers may not be able to discriminate very close tones, so that multiple matches may be reported even for tones whose descriptions are not strictly identical.

<div class="alert"><b>Note</b>  <b>TSPI_lineMonitorTones</b> is also used to detect silence. Silence is specified as a tone with all zero frequencies.</div>
<div> </div>
The corresponding function at the TAPI level does not include a <i>dwToneListID</i> parameter. The inclusion of this parameter at the TSPI interface allows TAPI to forward the union of all tone monitoring lists from all applications to the service provider, while still retaining the ability to filter and forward the tone detection events according to application. This gives service-provider designers the maximum flexibility to determine the degree to which they can discriminate very close tones, because TAPI makes no assumptions about what tone descriptions are considered identical.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemonitortone">LINEMONITORTONE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725234(v=vs.85)">LINE_MONITORTONE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>