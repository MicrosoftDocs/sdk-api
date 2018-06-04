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

# _DXVAHD_CUSTOM_RATE_DATA structure


## -description


Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC).


## -struct-fields




### -field CustomRate

The ratio of the output frame rate to the input frame rate, expressed as a <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure that holds a rational number.


### -field OutputFrames

The number of output frames that will be generated for every <i>N</i> input samples, where <i>N</i> = <b>InputFramesOrFields</b>.


### -field InputInterlaced


            If <b>TRUE</b>, the input stream must be interlaced<b></b>. Otherwise, the input stream must be progressive.


### -field InputFramesOrFields

The number of input fields or frames for every <i>N</i> output frames that will be generated, where <i>N</i> = <b>OutputFrames</b>.


## -remarks



The <b>CustomRate</b> member gives the rate conversion factor, while the remaining members define the pattern of input and output samples. 

Here are some example uses for this structure:

<ul>
<li>
Frame rate conversion from 60p to 120p (doubling the frame rate).

<ul>
<li><b>CustomRate</b>: 2/1</li>
<li><b>OutputFrames</b>: 2</li>
<li><b>InputInterlaced</b>: <b>FALSE</b></li>
<li><b>InputFramesOrFields</b>: 1</li>
</ul>
</li>
<li>
Reverse 2:3 pulldown (IVTC) from 60i to 24p.

<ul>
<li><b>CustomRate</b>: 4/5</li>
<li><b>OutputFrames</b>: 4</li>
<li><b>InputInterlaced</b>: <b>TRUE</b></li>
<li><b>InputFramesOrFields</b>: 10</li>
</ul>
(Ten interlaced fields are converted into four progressive frames.)

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

