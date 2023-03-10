---
UID: NS:qossp._AD_GENERAL_PARAMS
title: AD_GENERAL_PARAMS (qossp.h)
description: The AD_GENERAL_PARAMS structure contains the General Characterization Parameters contained in the RSVP Adspec object.
helpviewer_keywords: ["*LPAD_GENERAL_PARAMS","*LPAD_GENERAL_PARAMS structure [QOS]","AD_FLAG_BREAK_BIT","AD_GENERAL_PARAMS","AD_GENERAL_PARAMS structure [QOS]","qos.ad_general_params","qossp/*LPAD_GENERAL_PARAMS","qossp/AD_GENERAL_PARAMS"]
old-location: qos\ad_general_params.htm
tech.root: QOS
ms.assetid: eab6b317-9d06-45e2-bc77-0882f40e7d79
ms.date: 12/05/2018
ms.keywords: '*LPAD_GENERAL_PARAMS, *LPAD_GENERAL_PARAMS structure [QOS], AD_FLAG_BREAK_BIT, AD_GENERAL_PARAMS, AD_GENERAL_PARAMS structure [QOS], qos.ad_general_params, qossp/*LPAD_GENERAL_PARAMS, qossp/AD_GENERAL_PARAMS'
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AD_GENERAL_PARAMS, *LPAD_GENERAL_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AD_GENERAL_PARAMS
 - qossp/_AD_GENERAL_PARAMS
 - LPAD_GENERAL_PARAMS
 - qossp/LPAD_GENERAL_PARAMS
 - AD_GENERAL_PARAMS
 - qossp/AD_GENERAL_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - AD_GENERAL_PARAMS
---

# AD_GENERAL_PARAMS structure


## -description

The <b>AD_GENERAL_PARAMS</b> structure contains the General Characterization Parameters contained in the RSVP Adspec object.

## -struct-fields

### -field IntServAwareHopCount

Number of hops that conform to Integrated Services (INTSERV) requirements.

### -field PathBandwidthEstimate

Minimum bandwidth available from sender to receiver.

### -field MinimumLatency

Sum of the minimum latency of the packet forwarding process in routers, in milliseconds. Can be set to INDETERMINATE_LATENCY.

### -field PathMTU

Maximum Transmission Unit (MTU) for the end-to-end path between sender and receiver that will not incur packet fragmentation.

### -field Flags

Flags associated with the parameters. The following flag is supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AD_FLAG_BREAK_BIT"></a><a id="ad_flag_break_bit"></a><dl>
<dt><b>AD_FLAG_BREAK_BIT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the existence of a network element in the data path that does not support QOS control services. When set in a specific service override, indicates QOS service was not supported on at least one hop.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_adspec">RSVP_ADSPEC</a>