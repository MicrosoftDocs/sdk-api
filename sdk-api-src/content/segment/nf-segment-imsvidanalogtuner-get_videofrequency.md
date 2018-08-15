---
UID: NF:segment.IMSVidAnalogTuner.get_VideoFrequency
title: IMSVidAnalogTuner::get_VideoFrequency
author: windows-sdk-content
description: The get_VideoFrequency method retrieves the tuner's video frequency for testing purposes.
old-location: mstv\imsvidanalogtuner_get_videofrequency.htm
old-project: mstv
ms.assetid: c6ed5c47-c2cb-4025-9b93-57db25b5cec5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_VideoFrequency method, IMSVidAnalogTuner.get_VideoFrequency, IMSVidAnalogTuner::get_VideoFrequency, IMSVidAnalogTunerget_VideoFrequency, get_VideoFrequency, get_VideoFrequency method [Microsoft TV Technologies], get_VideoFrequency method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_videofrequency, segment/IMSVidAnalogTuner::get_VideoFrequency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.redist: 
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAnalogTuner.get_VideoFrequency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidAnalogTuner::get_VideoFrequency


## -description


The <b>get_VideoFrequency</b> method retrieves the tuner's video frequency for testing purposes.


## -parameters




### -param lcc






#### - plcc [out]

Pointer to a variable that receives the video frequency, in hertz (Hz).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is intended for diagnostic and testing purposes.




## -see-also




<a href="https://msdn.microsoft.com/d19552ce-1314-4217-9bd3-72369b4334cf">IAMTVTuner::get_VideoFrequency</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>
 

 

