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

# __MIDL___MIDL_itf_msrdc_0000_0000_0005 structure


## -description


The <b>RdcBufferPointer</b> structure describes a 
    buffer.


## -struct-fields




### -field m_Size

Size, in bytes, of the buffer.


### -field m_Used

For input buffers, <a href="https://msdn.microsoft.com/cc98a90c-ba82-4b92-a56c-07496a843089">IRdcComparator::Process</a> 
      and <a href="https://msdn.microsoft.com/34d19eee-0fa9-4ac3-a33b-9f01cfa06371">IRdcGenerator::Process</a> will store here how 
      much (if any) of the buffer was used during processing.


### -field m_Data

Pointer to the buffer.


## -see-also




<a href="https://msdn.microsoft.com/5144a94b-4af8-4ac2-b5b3-f0674a51c03b">Remote Differential Compression Structures</a>
 

 

