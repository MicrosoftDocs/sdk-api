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

# _MF_QUALITY_LEVEL enumeration


## -description


Specifies the quality level for a pipeline component. The quality level determines how the component consumes or produces samples.


## -enum-fields




### -field MF_QUALITY_NORMAL


            Normal quality.
          


### -field MF_QUALITY_NORMAL_MINUS_1


            One level below normal quality.
          


### -field MF_QUALITY_NORMAL_MINUS_2


            Two levels below normal quality.
          


### -field MF_QUALITY_NORMAL_MINUS_3


            Three levels below normal quality.
          


### -field MF_QUALITY_NORMAL_MINUS_4


            Four levels below normal quality.
          


### -field MF_QUALITY_NORMAL_MINUS_5


            Five levels below normal quality.
          


### -field MF_NUM_QUALITY_LEVELS


            Maximum number of quality levels. This value is not a valid flag.
          


## -remarks




        Each successive quality level decreases the amount of processing that is needed, while also reducing the resulting quality of the audio or video. The specific algorithm used to reduce quality depends on the component. Mode 1 is the least aggressive mode, and mode 5 is the most aggressive. A component is not required to implement all five levels. Also, the same quality level might not be comparable between two different components.
      


        Video decoders can often reduce quality by leaving out certain post-processing steps. The enhanced video renderer (EVR) can sometimes reduce quality by switching to a different deinterlacing mode.
      




## -see-also




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

