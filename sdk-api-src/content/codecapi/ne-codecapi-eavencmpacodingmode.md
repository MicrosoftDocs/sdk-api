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

# eAVEncMPACodingMode enumeration


## -description



Specifies the MPEG audio encoding mode. This enumeration is used with the <a href="https://msdn.microsoft.com/c1a303fd-3625-4051-b6b8-4f83cceec945">AVEncMPACodingMode</a> property.




## -enum-fields




### -field eAVEncMPACodingMode_Mono


            Single channel.
          This mode corresponds to single_channel mode (bit code '11'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_Stereo


            Stereo channels.
          This mode corresponds to stereo mode ('00'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_DualChannel


            Two mono channels.
          This mode corresponds to dual_channel mode ('10'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_JointStereo

Joint stereo mode. This mode uses similarities between the two channels to achieve greater compression. This mode corresponds to joint_stereo mode ('01'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_Surround


            Surround audio (5.1 channels).
          This mode applies to MPEG-2 audio (ISO/IEC 13818-3).


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

