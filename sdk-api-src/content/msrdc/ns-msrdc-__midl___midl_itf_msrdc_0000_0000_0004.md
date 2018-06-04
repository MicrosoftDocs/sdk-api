---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0004 structure


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
 

 

