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

# _MFNominalRange enumeration


## -description


Specifies whether color data includes headroom and toeroom. Headroom allows for values beyond 1.0 white ("whiter than white"), and toeroom allows for values below reference 0.0 black ("blacker than black").
        
      


## -enum-fields




### -field MFNominalRange_Unknown


            Unknown nominal range.
          


### -field MFNominalRange_Normal


            Equivalent to MFNominalRange_0_255.
          


### -field MFNominalRange_Wide


            Equivalent to MFNominalRange_16_235.
          


### -field MFNominalRange_0_255


            The normalized range [0...1] maps to [0...255] for 8-bit samples or [0...1023] for 10-bit samples.
          


### -field MFNominalRange_16_235


            The normalized range [0...1] maps to [16...235] for 8-bit samples or [64...940] for 10-bit samples.
          


### -field MFNominalRange_48_208


            The normalized range [0..1] maps to [48...208] for 8-bit samples or [64...940] for 10-bit samples.
          


### -field MFNominalRange_64_127

The normalized range [0..1] maps to [64...127] for 8-bit samples or [256...508] for 10-bit samples. This range is used in the xRGB color space.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFNominalRange_Last


### -field MFNominalRange_ForceDWORD




## -remarks




        This enumeration is used with the <a href="https://msdn.microsoft.com/7b2b809e-aae4-401c-816a-626fb88f5f87">MF_MT_VIDEO_NOMINAL_RANGE</a> attribute.
      


        For more information about these values, see the remarks for the <a href="https://msdn.microsoft.com/ebc146e4-517f-4413-93dc-66cf4b3a04c3">DXVA2_NominalRange</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.
      




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

