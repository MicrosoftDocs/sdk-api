---
UID: NS:rtmv2._RTM_ENTITY_ID
title: "_RTM_ENTITY_ID"
author: windows-sdk-content
description: The RTM_ENTITY_ID structure is used to uniquely identify a client to the routing table manager. The protocol identifier and the instance identifier are the values that are used to uniquely identify a client.
old-location: rras\rtm_entity_id.htm
tech.root: RRAS
ms.assetid: 6c75fb17-60b9-44cb-a934-430a6de74ee7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PRTM_ENTITY_ID, PRTM_ENTITY_ID, PRTM_ENTITY_ID structure pointer [RAS], RTM_ENTITY_ID, RTM_ENTITY_ID structure [RAS], _RTM_ENTITY_ID, _rtmv2ref_rtm_entity_id, rras.rtm_entity_id, rtmv2/PRTM_ENTITY_ID, rtmv2/RTM_ENTITY_ID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_ENTITY_ID
product: Windows
targetos: Windows
req.typenames: RTM_ENTITY_ID, *PRTM_ENTITY_ID
req.redist: 
---

# _RTM_ENTITY_ID structure


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




<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a>
 

 

