---
UID: NS:traffic._TC_GEN_FLOW
title: TC_GEN_FLOW (traffic.h)
description: The TC_GEN_FLOW structure creates a generic flow for use with the traffic control interface. The flow is customized through the members of this structure.
helpviewer_keywords: ["*PTC_GEN_FLOW","PTC_GEN_FLOW","PTC_GEN_FLOW structure pointer [QOS]","TC_GEN_FLOW","TC_GEN_FLOW structure [QOS]","_gqos_tc_gen_flow","qos.tc_gen_flow","traffic/PTC_GEN_FLOW","traffic/TC_GEN_FLOW"]
old-location: qos\tc_gen_flow.htm
tech.root: QOS
ms.assetid: 88b162d9-003c-42ce-8f82-91ee1aa9e32e
ms.date: 12/05/2018
ms.keywords: '*PTC_GEN_FLOW, PTC_GEN_FLOW, PTC_GEN_FLOW structure pointer [QOS], TC_GEN_FLOW, TC_GEN_FLOW structure [QOS], _gqos_tc_gen_flow, qos.tc_gen_flow, traffic/PTC_GEN_FLOW, traffic/TC_GEN_FLOW'
req.header: traffic.h
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
req.typenames: TC_GEN_FLOW, *PTC_GEN_FLOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TC_GEN_FLOW
 - traffic/_TC_GEN_FLOW
 - PTC_GEN_FLOW
 - traffic/PTC_GEN_FLOW
 - TC_GEN_FLOW
 - traffic/TC_GEN_FLOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - TC_GEN_FLOW
---

# TC_GEN_FLOW structure


## -description

The 
<b>TC_GEN_FLOW</b> structure creates a generic flow for use with the traffic control interface. The flow is customized through the members of this structure.

## -struct-fields

### -field SendingFlowspec

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure for the sending direction of the flow.

### -field ReceivingFlowspec

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure for the receiving direction of the flow.

### -field TcObjectsLength

Length of <b>TcObjects</b>, in bytes.

### -field TcObjects

Buffer that contains an array of traffic control objects specific to the given flow. The <b>TcObjects</b> member can contain objects from the list of currently supported objects. Definitions of these objects can be found in Qos.h and Traffic.h: 





<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_ds_class">QOS_DS_CLASS</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_traffic_class">QOS_TRAFFIC_CLASS</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_diffserv">QOS_DIFFSERV</a>



<a href="/windows/desktop/api/qos/ns-qos-qos_sd_mode">QOS_SD_MODE</a>



<a href="/windows/desktop/api/qos/ns-qos-qos_shaping_rate">QOS_SHAPING_RATE</a>


QOS_OBJECT_END_OF_LIST

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_diffserv">QOS_DIFFSERV</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_ds_class">QOS_DS_CLASS</a>



<a href="/windows/desktop/api/qos/ns-qos-qos_sd_mode">QOS_SD_MODE</a>



<a href="/windows/desktop/api/qos/ns-qos-qos_shaping_rate">QOS_SHAPING_RATE</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_traffic_class">QOS_TRAFFIC_CLASS</a>