---
UID: NS:winnt._NUMA_NODE_RELATIONSHIP
title: NUMA_NODE_RELATIONSHIP (winnt.h)
author: windows-sdk-content
description: Represents information about a NUMA node in a processor group. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\numa_node_relationship.htm
tech.root: ProcThread
ms.assetid: a4e4c994-c4af-4b4f-8684-6037bcba35a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PNUMA_NODE_RELATIONSHIP, NUMA_NODE_RELATIONSHIP, NUMA_NODE_RELATIONSHIP structure, PNUMA_NODE_RELATIONSHIP, PNUMA_NODE_RELATIONSHIP structure pointer, _NUMA_NODE_RELATIONSHIP, base.numa_node_relationship, winnt/NUMA_NODE_RELATIONSHIP, winnt/PNUMA_NODE_RELATIONSHIP'
ms.topic: struct
f1_keywords:
- winnt/NUMA_NODE_RELATIONSHIP
dev_langs:
 - c++
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
- NUMA_NODE_RELATIONSHIP
targetos: Windows
req.typenames: NUMA_NODE_RELATIONSHIP, *PNUMA_NODE_RELATIONSHIP
req.redist: 
ms.custom: 19H1
---

# NUMA_NODE_RELATIONSHIP structure


## -description


Represents information about a NUMA node in a processor group. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field NodeNumber

The number of the NUMA node.


### -field Reserved

This member is reserved.


### -field GroupMask

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a> structure that specifies a  group number and processor affinity within the group. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a>



<a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

