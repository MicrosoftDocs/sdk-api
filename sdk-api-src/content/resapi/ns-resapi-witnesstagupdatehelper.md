---
UID: NS:resapi._WitnessTagUpdateHelper
title: WitnessTagUpdateHelper (resapi.h)
description: Contains information used to update and validate a PaxosTagCStruct structure.
helpviewer_keywords: ["WitnessTagUpdateHelper","WitnessTagUpdateHelper structure [Failover Cluster]","mscs.witnesstagupdatehelper","resapi/WitnessTagUpdateHelper"]
old-location: mscs\witnesstagupdatehelper.htm
tech.root: MsCS
ms.assetid: 4737A2B0-E295-49B6-8A84-D38BC317011B
ms.date: 12/05/2018
ms.keywords: WitnessTagUpdateHelper, WitnessTagUpdateHelper structure [Failover Cluster], mscs.witnesstagupdatehelper, resapi/WitnessTagUpdateHelper
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
req.typenames: WitnessTagUpdateHelper
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WitnessTagUpdateHelper
 - resapi/_WitnessTagUpdateHelper
 - WitnessTagUpdateHelper
 - resapi/WitnessTagUpdateHelper
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
 - WitnessTagUpdateHelper
---

# WitnessTagUpdateHelper structure


## -description

Contains information used to update and validate a <a href="/windows/desktop/api/resapi/ns-resapi-paxostagcstruct">PaxosTagCStruct</a> structure.

## -struct-fields

### -field Version

The cluster configuration version to validate.

### -field paxosToSet

The Paxos tag to update.

### -field paxosToValidate

The Paxos tag to validate.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>



<a href="/windows/desktop/api/resapi/ns-resapi-witnesstagupdatehelper">WitnessTagUpdateHelper</a>