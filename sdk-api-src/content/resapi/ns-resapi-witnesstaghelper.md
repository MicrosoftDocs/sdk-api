---
UID: NS:resapi._WitnessTagHelper
title: WitnessTagHelper (resapi.h)
description: Contains information used to validate a PaxosTagCStruct structure.
helpviewer_keywords: ["PWitnessTagHelper","PWitnessTagHelper structure pointer [Failover Cluster]","WitnessTagHelper","WitnessTagHelper structure [Failover Cluster]","mscs.witnesstaghelper","resapi/PWitnessTagHelper","resapi/WitnessTagHelper"]
old-location: mscs\witnesstaghelper.htm
tech.root: MsCS
ms.assetid: FFE7EF63-4025-4CC5-B3F8-FF07FA67AFD1
ms.date: 12/05/2018
ms.keywords: PWitnessTagHelper, PWitnessTagHelper structure pointer [Failover Cluster], WitnessTagHelper, WitnessTagHelper structure [Failover Cluster], mscs.witnesstaghelper, resapi/PWitnessTagHelper, resapi/WitnessTagHelper
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: WitnessTagHelper
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WitnessTagHelper
 - resapi/_WitnessTagHelper
 - WitnessTagHelper
 - resapi/WitnessTagHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - WitnessTagHelper
---

# WitnessTagHelper structure


## -description

Contains information used to validate a <a href="/windows/desktop/api/resapi/ns-resapi-paxostagcstruct">PaxosTagCStruct</a> structure.

## -struct-fields

### -field Version

The cluster configuration version to validate.

### -field paxosToValidate

The Paxos tag to validate.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>



<a href="/windows/desktop/api/resapi/ns-resapi-witnesstagupdatehelper">WitnessTagUpdateHelper</a>