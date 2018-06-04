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

# tagVideoProcAmpProperty enumeration


## -description



The <b>VideoProcAmpProperty</b> enumeration specifies video properties on a video capture device.




## -enum-fields




### -field VideoProcAmp_Brightness


            Specifies the brightness, also called the <i>black level</i>. For NTSC, the value is expressed in IRE units * 100. For non-NTSC sources, the units are arbitrary, with zero representing blanking and 10,000 representing pure white. Values range from –10,000 to 10,000.
          


### -field VideoProcAmp_Contrast


            Specifies the contrast, expressed as gain factor * 100. Values range from zero to 10,000.
          


### -field VideoProcAmp_Hue


            Specifies the hue, in degrees * 100. Values range from -180,000 to 180,000 (-180 to +180 degrees).
          


### -field VideoProcAmp_Saturation


            Specifies the saturation. Values range from 0 to 10,000.
          


### -field VideoProcAmp_Sharpness


            Specifies the sharpness. Values range from 0 to 100.
          


### -field VideoProcAmp_Gamma


            Specifies the gamma, as gamma * 100. Values range from 1 to 500.
          


### -field VideoProcAmp_ColorEnable


            Specifies the color enable setting. The possible values are 0 (off) and 1 (on).
          


### -field VideoProcAmp_WhiteBalance


            Specifies the white balance, as a color temperature in degrees Kelvin. The range of values depends on the device.
          


### -field VideoProcAmp_BacklightCompensation


            Specifies the backlight compensation setting. Possible values are 0 (off) and 1 (on).
          


### -field VideoProcAmp_Gain


            Specifies the gain adjustment. Zero is normal. Positive values are brighter and negative values are darker. The range of values depends on the device.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/28c45790-2e5a-4acb-8a53-93f19c51dc6a">IAMVideoProcAmp</a>
 

 

