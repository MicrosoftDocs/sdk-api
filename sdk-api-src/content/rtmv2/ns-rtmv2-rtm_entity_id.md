---
UID: NS:rtmv2._RTM_ENTITY_ID
title: RTM_ENTITY_ID (rtmv2.h)
description: The RTM_ENTITY_ID structure is used to uniquely identify a client to the routing table manager. The protocol identifier and the instance identifier are the values that are used to uniquely identify a client.
helpviewer_keywords: ["*PRTM_ENTITY_ID","PRTM_ENTITY_ID","PRTM_ENTITY_ID structure pointer [RAS]","RTM_ENTITY_ID","RTM_ENTITY_ID structure [RAS]","_rtmv2ref_rtm_entity_id","rras.rtm_entity_id","rtmv2/PRTM_ENTITY_ID","rtmv2/RTM_ENTITY_ID"]
old-location: rras\rtm_entity_id.htm
tech.root: RRAS
ms.assetid: 6c75fb17-60b9-44cb-a934-430a6de74ee7
ms.date: 12/05/2018
ms.keywords: '*PRTM_ENTITY_ID, PRTM_ENTITY_ID, PRTM_ENTITY_ID structure pointer [RAS], RTM_ENTITY_ID, RTM_ENTITY_ID structure [RAS], _rtmv2ref_rtm_entity_id, rras.rtm_entity_id, rtmv2/PRTM_ENTITY_ID, rtmv2/RTM_ENTITY_ID'
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: RTM_ENTITY_ID, *PRTM_ENTITY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_ENTITY_ID
 - rtmv2/_RTM_ENTITY_ID
 - PRTM_ENTITY_ID
 - rtmv2/PRTM_ENTITY_ID
 - RTM_ENTITY_ID
 - rtmv2/RTM_ENTITY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_ENTITY_ID
---

# RTM_ENTITY_ID structure


## -description

The 
<b>RTM_ENTITY_ID</b> structure is used to uniquely identify a client to the routing table manager. The protocol identifier and the instance identifier are the values that are used to uniquely identify a client.

## -struct-fields

### -field EntityProtocolId

Specifies a client's protocol identifier (such as RIP or OSPF).

### -field EntityInstanceId

Specifies a client's protocol instance (such as RIPv1 or RIPv2).

### -field EntityId

Specifies a client's identifier, which is a combination of the <b>EntityProtocolId</b> and the <b>EntityInstanceId</b>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a>