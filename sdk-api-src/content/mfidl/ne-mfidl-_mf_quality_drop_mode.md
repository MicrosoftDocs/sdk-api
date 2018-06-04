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

# _MF_QUALITY_DROP_MODE enumeration


## -description



Specifies how aggressively a pipeline component should drop samples.




## -enum-fields




### -field MF_DROP_MODE_NONE

Normal processing of samples. Drop mode is disabled.


### -field MF_DROP_MODE_1

First drop mode (least aggressive).


### -field MF_DROP_MODE_2

Second drop mode.


### -field MF_DROP_MODE_3

Third drop mode.


### -field MF_DROP_MODE_4

Fourth drop mode.


### -field MF_DROP_MODE_5

Fifth drop mode (most aggressive, if it is supported; see Remarks).


### -field MF_NUM_DROP_MODES

Maximum number of drop modes. This value is not a valid flag.


## -remarks



In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode. The specific algorithm used depends on the component. Mode 1 is the least aggressive mode, and mode 5 is the most aggressive. A component is not required to implement all five levels.

For example, suppose an encoded video stream has three B-frames between each pair of P-frames. A decoder might implement the following drop modes:

<ul>
<li>
Mode 1: Drop one out of every three B frames.

</li>
<li>
Mode 2: Drop one out of every two B frames.

</li>
<li>
Mode 3: Drop all delta frames.

</li>
<li>
Modes 4 and 5: Unsupported.

</li>
</ul>
The enhanced video renderer (EVR) can drop video frames before sending them to the EVR mixer.




## -see-also




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

