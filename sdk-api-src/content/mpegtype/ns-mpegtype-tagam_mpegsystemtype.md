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

# tagAM_MPEGSYSTEMTYPE structure


## -description



          
          The <b>AM_MPEGSYSTEMTYPE</b> structure defines the format block for an MPEG-1 system stream. 
      This structure is used when the <b>formattype</b> member of the <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure is FORMAT_MPEG1System.
        


## -struct-fields




### -field dwBitRate

Bits per second.


### -field cStreams

Number of streams.


### -field Streams


              List <a href="https://msdn.microsoft.com/8622ffcb-be64-4a8f-8bc7-834b559b0f95">AM_MPEGSTREAMTYPE</a> structures that describe the elementary streams. The number of elements in the list is given by the <b>cStream</b> member. The size of each <b>AM_MPEGSTREAMTYPE</b> structure is variable. Use the <b>AM_MPEGSTREAMTYPE_ELEMENTLENGTH</b> macro to calculate the size of each structure.


## -remarks



The <b>Streams</b> member contains a list of <a href="https://msdn.microsoft.com/8622ffcb-be64-4a8f-8bc7-834b559b0f95">AM_MPEGSTREAMTYPE</a> structures. The size of each <b>AM_MPEGSTREAMTYPE</b> structure is aligned to an 8-byte boundary. Given a pointer to an <b>AM_MPEGSTREAMTYPE</b> structure in list, use the <b>AM_MPEGSTREAMTYPE_NEXT</b> macro to get a pointer to the next structure.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8">MEPG-1 Media Types</a>
 

 

