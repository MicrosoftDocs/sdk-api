---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0004
title: RdcNeed
author: windows-sdk-content
description: Contains information about a chunk that is required to synchronize two sets of data.
old-location: rdc\rdcneed.htm
tech.root: rdc
ms.assetid: 086e82f1-b033-48e2-b648-895c04751cc9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RdcNeed, RdcNeed structure [Remote Differential Compression], fs.rdcneed, msrdc/RdcNeed, rdc.rdcneed
ms.topic: struct
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
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
 - MsRdc.h
api_name:
 - RdcNeed
product: Windows
targetos: Windows
req.typenames: RdcNeed
req.redist: 
---

# RdcNeed structure


## -description


The <b>RdcNeed</b> structure contains information about a 
    chunk that is required to synchronize two sets of data.


## -struct-fields




### -field m_BlockType

Describes the type of data needed—source data or seed data.


### -field m_FileOffset

Offset, in bytes, from the start of the data where the chunk should be copied from.


### -field m_BlockLength

Length, in bytes, of the chunk of data that is to be copied to the target data.


## -see-also




<a href="https://msdn.microsoft.com/92a1fae7-5ada-4f7d-a736-c93bc404a418">RdcNeedPointer</a>



<a href="https://msdn.microsoft.com/93173b2e-a0df-445e-98a8-f7df02fbc7a8">RdcNeedType</a>



<a href="https://msdn.microsoft.com/5144a94b-4af8-4ac2-b5b3-f0674a51c03b">Remote Differential Compression Structures</a>
 

 

