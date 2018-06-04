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
 

 

