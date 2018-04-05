---
UID: NS:winnt._GROUP_AFFINITY
title: "_GROUP_AFFINITY"
author: windows-driver-content
description: Represents a processor group-specific affinity, such as the affinity of a thread.
old-location: base\group_affinity.htm
old-project: ProcThread
ms.assetid: 76009431-9139-4c03-9c7b-0c4bb5f0cb83
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PGROUP_AFFINITY, GROUP_AFFINITY, GROUP_AFFINITY structure, PGROUP_AFFINITY, PGROUP_AFFINITY structure pointer, _GROUP_AFFINITY, base.group_affinity, winnt/GROUP_AFFINITY, winnt/PGROUP_AFFINITY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: GROUP_AFFINITY, *PGROUP_AFFINITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
api_name:
-	GROUP_AFFINITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _GROUP_AFFINITY structure


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




<a href="https://msdn.microsoft.com/f8fe521b-02d6-4c58-8ef8-653280add111">CACHE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/a4e4c994-c4af-4b4f-8684-6037bcba35a9">NUMA_NODE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/1efda80d-cf5b-4312-801a-ea3585b152ac">PROCESSOR_RELATIONSHIP</a>
 

 

