---
UID: NF:segment.IMSVidAnalogTuner.get_Channel
title: IMSVidAnalogTuner::get_Channel
author: windows-driver-content
description: The get_Channel method retrieves the tuner's current channel.
old-location: mstv\imsvidanalogtuner_get_channel.htm
old-project: mstv
ms.assetid: 9d62cd70-02cf-4454-b5b7-da2d623ec95d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_Channel method, IMSVidAnalogTuner.get_Channel, IMSVidAnalogTuner::get_Channel, IMSVidAnalogTunerget_Channel, get_Channel, get_Channel method [Microsoft TV Technologies], get_Channel method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_channel, segment/IMSVidAnalogTuner::get_Channel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidAnalogTuner.get_Channel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidAnalogTuner::get_Channel


## -description


The <b>get_Channel</b> method retrieves the tuner's current channel.


## -parameters




### -param Channel






#### - pChannel [out]

Pointer to a variable that receives the channel.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/68c1b6da-4380-4831-b554-bbb2e3e55ef9">IAMTuner::get_Channel</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>



<a href="https://msdn.microsoft.com/1afd718d-bca9-478c-b56e-413de0f15656">IMSVidAnalogTuner::put_Channel</a>
 

 

