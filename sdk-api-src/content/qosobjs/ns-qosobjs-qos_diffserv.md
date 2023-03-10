---
UID: NS:qosobjs._QOS_DIFFSERV
title: QOS_DIFFSERV (qosobjs.h)
description: The QOS_DIFFSERV traffic control object is used to specify filters for the packet scheduler when it operates in Differentiated Services Mode.
helpviewer_keywords: ["*LPQOS_DIFFSERV","LPQOS_DIFFSERV","LPQOS_DIFFSERV structure pointer [QOS]","QOS_DIFFSERV","QOS_DIFFSERV structure [QOS]","_gqos_qos_diffserv","qos.qos_diffserv","qosobjs/LPQOS_DIFFSERV","qosobjs/QOS_DIFFSERV"]
old-location: qos\qos_diffserv.htm
tech.root: QOS
ms.assetid: 3d1035dc-0e46-46f4-abb3-26100356b60d
ms.date: 12/05/2018
ms.keywords: '*LPQOS_DIFFSERV, LPQOS_DIFFSERV, LPQOS_DIFFSERV structure pointer [QOS], QOS_DIFFSERV, QOS_DIFFSERV structure [QOS], _gqos_qos_diffserv, qos.qos_diffserv, qosobjs/LPQOS_DIFFSERV, qosobjs/QOS_DIFFSERV'
req.header: qosobjs.h
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
req.typenames: QOS_DIFFSERV, *LPQOS_DIFFSERV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_DIFFSERV
 - qosobjs/_QOS_DIFFSERV
 - LPQOS_DIFFSERV
 - qosobjs/LPQOS_DIFFSERV
 - QOS_DIFFSERV
 - qosobjs/QOS_DIFFSERV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - QosObjs.h
api_name:
 - QOS_DIFFSERV
---

# QOS_DIFFSERV structure


## -description

The 
<b>QOS_DIFFSERV</b> traffic control object is used to specify filters for the packet scheduler when it operates in Differentiated Services Mode.

## -struct-fields

### -field ObjectHdr

The QOS object 
<b>QOS_OBJECT_HDR</b>. The object type for this traffic control object should be 
QOS_OBJECT_DIFFSERV.

### -field DSFieldCount

Number of Diffserv Rules in this object.

### -field DiffservRule

Array of 
<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_diffserv_rule">QOS_DIFFSERV_RULE</a> structures.

## -remarks

The 
<b>QOS_DIFFSERV</b> object is used to specify the set of Diffserv rules that apply to the specified flow, all of which are specified in the <b>DiffservRule</b> member. Each Diffserv rule has an InboundDSField value, which signifies the DSCP on the Inbound packet. The Diffserv Rules also have OutboundDSCP and UserPriority values for conforming and nonconforming packets. These indicate the DSCP and 802.1p values that go out on the forwarded packet. Note that the DSCP or UserPriority mapping based on ServiceType or 
<b>QOS_DS_CLASS</b> or 
<b>QOS_TRAFFIC_CLASS</b> is not used in this mode.

## -see-also

<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_diffserv_rule">QOS_DIFFSERV_RULE</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_ds_class">QOS_DS_CLASS</a>



<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_traffic_class">QOS_TRAFFIC_CLASS</a>