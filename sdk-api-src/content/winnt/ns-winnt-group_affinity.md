---
UID: NS:winnt._GROUP_AFFINITY
title: GROUP_AFFINITY (winnt.h)
description: Represents a processor group-specific affinity, such as the affinity of a thread.
helpviewer_keywords: ["*PGROUP_AFFINITY","GROUP_AFFINITY","GROUP_AFFINITY structure","PGROUP_AFFINITY","PGROUP_AFFINITY structure pointer","base.group_affinity","winnt/GROUP_AFFINITY","winnt/PGROUP_AFFINITY"]
old-location: base\group_affinity.htm
tech.root: backup
ms.assetid: 76009431-9139-4c03-9c7b-0c4bb5f0cb83
ms.date: 12/05/2018
ms.keywords: '*PGROUP_AFFINITY, GROUP_AFFINITY, GROUP_AFFINITY structure, PGROUP_AFFINITY, PGROUP_AFFINITY structure pointer, base.group_affinity, winnt/GROUP_AFFINITY, winnt/PGROUP_AFFINITY'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: GROUP_AFFINITY, *PGROUP_AFFINITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_AFFINITY
 - winnt/_GROUP_AFFINITY
 - PGROUP_AFFINITY
 - winnt/PGROUP_AFFINITY
 - GROUP_AFFINITY
 - winnt/GROUP_AFFINITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - GROUP_AFFINITY
---

# GROUP_AFFINITY structure


## -description

Represents a processor group-specific affinity, such as the affinity of a thread.

## -struct-fields

### -field Mask

A bitmap that specifies the affinity for zero or more processors within the specified group.

### -field Group

The processor group number.

### -field Reserved

This member is reserved.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-cache_relationship">CACHE_RELATIONSHIP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-numa_node_relationship">NUMA_NODE_RELATIONSHIP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-processor_relationship">PROCESSOR_RELATIONSHIP</a>