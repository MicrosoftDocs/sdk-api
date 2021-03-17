---
UID: NS:rtmv2._RTM_ENTITY_INFO
title: RTM_ENTITY_INFO (rtmv2.h)
description: The RTM_ENTITY_INFO structure is used to exchange client information with the routing table manager.
helpviewer_keywords: ["*PRTM_ENTITY_INFO","PRTM_ENTITY_INFO","PRTM_ENTITY_INFO structure pointer [RAS]","RTM_ENTITY_INFO","RTM_ENTITY_INFO structure [RAS]","_rtmv2ref_rtm_entity_info","rras.rtm_entity_info","rtmv2/PRTM_ENTITY_INFO","rtmv2/RTM_ENTITY_INFO"]
old-location: rras\rtm_entity_info.htm
tech.root: RRAS
ms.assetid: b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a
ms.date: 12/05/2018
ms.keywords: '*PRTM_ENTITY_INFO, PRTM_ENTITY_INFO, PRTM_ENTITY_INFO structure pointer [RAS], RTM_ENTITY_INFO, RTM_ENTITY_INFO structure [RAS], _rtmv2ref_rtm_entity_info, rras.rtm_entity_info, rtmv2/PRTM_ENTITY_INFO, rtmv2/RTM_ENTITY_INFO'
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
req.typenames: RTM_ENTITY_INFO, *PRTM_ENTITY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_ENTITY_INFO
 - rtmv2/_RTM_ENTITY_INFO
 - PRTM_ENTITY_INFO
 - rtmv2/PRTM_ENTITY_INFO
 - RTM_ENTITY_INFO
 - rtmv2/RTM_ENTITY_INFO
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
 - RTM_ENTITY_INFO
---

# RTM_ENTITY_INFO structure


## -description

The 
<b>RTM_ENTITY_INFO</b> structure is used to exchange client information with the routing table manager.

## -struct-fields

### -field RtmInstanceId

Specifies the instance of the routing table manager with which the client registered.

### -field AddressFamily

Specifies the address family to which the client belongs.

### -field EntityId

Specifies the identifier that uniquely identifies a client.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_id">RTM_ENTITY_ID</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetentityinfo">RtmGetEntityInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetregisteredentities">RtmGetRegisteredEntities</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentityinfo">RtmReleaseEntityInfo</a>