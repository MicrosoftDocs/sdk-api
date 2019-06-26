---
UID: NS:winnt._GROUP_AFFINITY
title: GROUP_AFFINITY (winnt.h)
author: windows-sdk-content
description: Represents a processor group-specific affinity, such as the affinity of a thread.
old-location: base\group_affinity.htm
tech.root: ProcThread
ms.assetid: 76009431-9139-4c03-9c7b-0c4bb5f0cb83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PGROUP_AFFINITY, GROUP_AFFINITY, GROUP_AFFINITY structure, PGROUP_AFFINITY, PGROUP_AFFINITY structure pointer, base.group_affinity, winnt/GROUP_AFFINITY, winnt/PGROUP_AFFINITY"
ms.topic: struct
f1_keywords: 
 - "winnt/GROUP_AFFINITY"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - GROUP_AFFINITY
product: Windows
targetos: Windows
req.typenames: GROUP_AFFINITY, *PGROUP_AFFINITY
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_cache_relationship">CACHE_RELATIONSHIP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_numa_node_relationship">NUMA_NODE_RELATIONSHIP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_processor_relationship">PROCESSOR_RELATIONSHIP</a>
 

 

