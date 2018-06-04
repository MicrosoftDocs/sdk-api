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

# _VMR9_SampleFormat enumeration


## -description



The <b>VMR9_SampleFormat</b> enumeration type describes the interlacing of a video stream.




## -enum-fields




### -field VMR9_SampleReserved


            Reserved; do not use.
          


### -field VMR9_SampleProgressiveFrame


            Progressive frame; no interleaving
          


### -field VMR9_SampleFieldInterleavedEvenFirst


            Each sample contains two interleaved fields, with the even field first.
          


### -field VMR9_SampleFieldInterleavedOddFirst


            Each sample contains two interleaved fields, with the odd field first.
          


### -field VMR9_SampleFieldSingleEven


            The sample contains a single field, and each line in the sample corresponds to the even lines in a deinterlaced frame. That is, lines 0, 1, 2,... in the sample correspond to lines 0, 2, 4,... in the deinterlaced frame. The missing lines must be constructed when the frame is deinterlaced.
          


### -field VMR9_SampleFieldSingleOdd


            The sample contains a single field, and each line in the sample corresponds to the odd lines in a de-interlaced frame.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/af4bf46a-fae7-4485-b5fb-3fd1857f383f">VMR9VideoDesc</a>



<a href="https://msdn.microsoft.com/e2da0c1e-d592-49ce-937c-0d75ce270282">VMR9VideoStreamInfo</a>
 

 

