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

# _MFVideoInterlaceMode enumeration


## -description


Specifies how a video stream is interlaced.

In the descriptions that follow, upper field refers to the field that contains the leading half scan line. Lower field refers to the field that contains the first full scan line.


## -enum-fields




### -field MFVideoInterlace_Unknown


            The type of interlacing is not known.
          


### -field MFVideoInterlace_Progressive


            Progressive frames.
          


### -field MFVideoInterlace_FieldInterleavedUpperFirst


            Interlaced frames. Each frame contains two fields. The field lines are interleaved, with the upper field appearing on the first line.
          


### -field MFVideoInterlace_FieldInterleavedLowerFirst


            Interlaced frames. Each frame contains two fields. The field lines are interleaved, with the lower field appearing on the first line.
          


### -field MFVideoInterlace_FieldSingleUpper


            Interlaced frames. Each frame contains one field, with the upper field appearing first.
          


### -field MFVideoInterlace_FieldSingleLower


            Interlaced frames. Each frame contains one field, with the lower field appearing first.
          


### -field MFVideoInterlace_MixedInterlaceOrProgressive


            The stream contains a mix of interlaced and progressive modes.
          


### -field MFVideoInterlace_Last


            Reserved.
          


### -field MFVideoInterlace_ForceDWORD


            Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.
          


## -remarks



Scan lines in the lower field are 0.5 scan line lower than those in the upper field. In NTSC television, a frame consists of a lower field followed by an upper field. In PAL television, a frame consists of an upper field followed by a lower field.

The upper field is also called the even field, the top field, or field 2. The lower field is also called the odd field, the bottom field, or field 1.

If the interlace mode is MFVideoInterlace_FieldSingleUpper or MFVideoInterlace_FieldSingleLower, each sample contains a single field, so each buffer contains only half the number of field lines given in the media type.




## -see-also




<a href="https://msdn.microsoft.com/19aa0147-ac49-4a2e-ac75-e967fec9ca68">MF_MT_INTERLACE_MODE</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/2911ae57-1703-4a9d-bd33-94af1e0f8804">Video Interlacing</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

