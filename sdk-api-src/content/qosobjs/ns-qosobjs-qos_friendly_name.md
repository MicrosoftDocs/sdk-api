---
UID: NS:qosobjs._QOS_FRIENDLY_NAME
title: QOS_FRIENDLY_NAME (qosobjs.h)
description: The QOS_FRIENDLY_NAME traffic control object associates a friendly name with flow.
helpviewer_keywords: ["*LPQOS_FRIENDLY_NAME","LPQOS_FRIENDLY_NAME","LPQOS_FRIENDLY_NAME structure pointer [QOS]","QOS_FRIENDLY_NAME","QOS_FRIENDLY_NAME structure [QOS]","_gqos_qos_friendly_name","qos.qos_friendly_name","qosobjs/LPQOS_FRIENDLY_NAME","qosobjs/QOS_FRIENDLY_NAME"]
old-location: qos\qos_friendly_name.htm
tech.root: QOS
ms.assetid: 9681fc36-0a31-4b2a-9719-085506126877
ms.date: 12/05/2018
ms.keywords: '*LPQOS_FRIENDLY_NAME, LPQOS_FRIENDLY_NAME, LPQOS_FRIENDLY_NAME structure pointer [QOS], QOS_FRIENDLY_NAME, QOS_FRIENDLY_NAME structure [QOS], _gqos_qos_friendly_name, qos.qos_friendly_name, qosobjs/LPQOS_FRIENDLY_NAME, qosobjs/QOS_FRIENDLY_NAME'
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
req.typenames: QOS_FRIENDLY_NAME, *LPQOS_FRIENDLY_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_FRIENDLY_NAME
 - qosobjs/_QOS_FRIENDLY_NAME
 - LPQOS_FRIENDLY_NAME
 - qosobjs/LPQOS_FRIENDLY_NAME
 - QOS_FRIENDLY_NAME
 - qosobjs/QOS_FRIENDLY_NAME
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
 - QOS_FRIENDLY_NAME
---

# QOS_FRIENDLY_NAME structure


## -description

The 
<b>QOS_FRIENDLY_NAME</b> traffic control object associates a friendly name with flow.

## -struct-fields

### -field ObjectHdr

The QOS object 
<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>. The object type for this traffic control object should be 
<b>QOS_OBJECT_FRIENDLY_NAME</b>.

### -field FriendlyName

Name to be associated with the flow.

## -remarks

Programmers are encouraged to use the 
<b>QOS_FRIENDLY_NAME</b> traffic control object to associate flows with their applications. This approach enables management applications to identify and associate enumerated flows with corresponding applications.

## -see-also

<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_diffserv_rule">QOS_DIFFSERV_RULE</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_ds_class">QOS_DS_CLASS</a>



<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>



<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_traffic_class">QOS_TRAFFIC_CLASS</a>