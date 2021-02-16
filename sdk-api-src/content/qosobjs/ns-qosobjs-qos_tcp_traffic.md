---
UID: NS:qosobjs._QOS_TCP_TRAFFIC
title: QOS_TCP_TRAFFIC (qosobjs.h)
description: The QOS_TCP_TRAFFIC structure is used to indicate that IP Precedence and UserPriority mappings for a given flow must be set to system defaults for TCP traffic.
helpviewer_keywords: ["*LPQOS_TCP_TRAFFIC","*LPQOS_TCP_TRAFFIC structure [QOS]","QOS_TCP_TRAFFIC","QOS_TCP_TRAFFIC structure [QOS]","qos.qos_tcp_traffic","qosobjs/*LPQOS_TCP_TRAFFIC","qosobjs/QOS_TCP_TRAFFIC"]
old-location: qos\qos_tcp_traffic.htm
tech.root: QOS
ms.assetid: e71b0414-d449-42af-9d28-d2ae9fa1b6ea
ms.date: 12/05/2018
ms.keywords: '*LPQOS_TCP_TRAFFIC, *LPQOS_TCP_TRAFFIC structure [QOS], QOS_TCP_TRAFFIC, QOS_TCP_TRAFFIC structure [QOS], qos.qos_tcp_traffic, qosobjs/*LPQOS_TCP_TRAFFIC, qosobjs/QOS_TCP_TRAFFIC'
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
req.typenames: QOS_TCP_TRAFFIC, *LPQOS_TCP_TRAFFIC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_TCP_TRAFFIC
 - qosobjs/_QOS_TCP_TRAFFIC
 - LPQOS_TCP_TRAFFIC
 - qosobjs/LPQOS_TCP_TRAFFIC
 - QOS_TCP_TRAFFIC
 - qosobjs/QOS_TCP_TRAFFIC
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
 - QOS_TCP_TRAFFIC
---

# QOS_TCP_TRAFFIC structure


## -description

The <b>QOS_TCP_TRAFFIC</b> structure is used to indicate that IP Precedence and UserPriority mappings for a given flow must be set to system defaults for TCP traffic.

## -struct-fields

### -field ObjectHdr

A QOS object header.

## -remarks

When the <b>QOS_TCP_TRAFFIC</b> object is passed, the <b>DSField</b> mapping and <b>UserPriorityMapping</b> of <b>ServiceType</b> are ignored, as are QOS_OBJECT_DS_CLASS and QOS_OBJECT_TRAFFIC_CLASS.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>