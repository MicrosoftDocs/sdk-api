---
UID: NF:segment.IMSVidAnalogTuner.get_AudioFrequency
title: IMSVidAnalogTuner::get_AudioFrequency method
author: windows-driver-content
description: The get_AudioFrequency method retrieves the tuner's audio frequency.
old-location: mstv\imsvidanalogtuner_get_audiofrequency.htm
old-project: mstv
ms.assetid: d0513ea0-305b-40ac-95ad-ed47a0417046
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidAnalogTuner, IMSVidAnalogTuner interface [Microsoft TV Technologies], get_AudioFrequency method, IMSVidAnalogTuner::get_AudioFrequency, IMSVidAnalogTunerget_AudioFrequency, get_AudioFrequency method [Microsoft TV Technologies], get_AudioFrequency method [Microsoft TV Technologies], IMSVidAnalogTuner interface, get_AudioFrequency,IMSVidAnalogTuner.get_AudioFrequency, mstv.imsvidanalogtuner_get_audiofrequency, segment/IMSVidAnalogTuner::get_AudioFrequency
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
-	IMSVidAnalogTuner.get_AudioFrequency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidAnalogTuner::get_AudioFrequency method


## -description


The <b>get_AudioFrequency</b> method retrieves the tuner's audio frequency.


## -parameters




### -param lcc






#### - plcc [out]

Pointer to a variable that receives the audio frequency, in hertz (Hz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is intended for diagnostic and testing purposes.




## -see-also




<a href="https://msdn.microsoft.com/7d0d288a-7ad0-40ad-b86e-9df9447ed484">IAMTVTuner::get_AudioFrequency</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>
 

 

