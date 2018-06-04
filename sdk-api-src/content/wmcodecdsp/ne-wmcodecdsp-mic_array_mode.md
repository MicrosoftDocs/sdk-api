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

# MIC_ARRAY_MODE enumeration


## -description


Specifies how the voice capture DSP performs microphone array processing. This enumeration is used with the <a href="https://msdn.microsoft.com/5e04fe50-d764-4497-9999-37279e156204">MFPKEY_WMAAECMA_FEATR_MICARR_MODE</a> property.


## -enum-fields




### -field MICARRAY_SINGLE_CHAN

Use a single channel. Specify the channel number in the last 8 bits of the value.


### -field MICARRAY_SIMPLE_SUM

Sum all of the channels.




### -field MICARRAY_SINGLE_BEAM

Use beam forming with a beam selected by the DSP. After processing starts, you can query which beam was selected by reading the <a href="https://msdn.microsoft.com/9ed761da-3f1b-47e8-b71f-becc56fe8801">MFPKEY_WMAAECMA_FEATR_MICARR_BEAM</a> property.


### -field MICARRAY_FIXED_BEAM

Use beam forming with the center beam.


### -field MICARRAY_EXTERN_BEAM

Use beam forming with a beam selected by the application. If you set this value, set the MFPKEY_WMAAECMA_FEATR_MICARR_BEAM property to specify the beam.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/6c77c8f6-289e-4130-b56a-e1f0bcc40f3e">Voice Capture</a>
 

 

