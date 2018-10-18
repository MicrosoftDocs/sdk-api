---
UID: NE:wmcodecdsp.MIC_ARRAY_MODE
title: MIC_ARRAY_MODE
author: windows-sdk-content
description: Specifies how the voice capture DSP performs microphone array processing. This enumeration is used with the MFPKEY_WMAAECMA_FEATR_MICARR_MODE property.
old-location: mf\mic_array_modeenumeration.htm
tech.root: medfound
ms.assetid: 95335d2e-94f9-4e8d-b578-a4d08055bb56
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: MICARRAY_EXTERN_BEAM, MICARRAY_FIXED_BEAM, MICARRAY_SIMPLE_SUM, MICARRAY_SINGLE_BEAM, MICARRAY_SINGLE_CHAN, MIC_ARRAY_MODE, MIC_ARRAY_MODE enumeration [Media Foundation], codecapi.mic_array_modeenumeration, mf.mic_array_modeenumeration, wmcodecdsp/MICARRAY_EXTERN_BEAM, wmcodecdsp/MICARRAY_FIXED_BEAM, wmcodecdsp/MICARRAY_SIMPLE_SUM, wmcodecdsp/MICARRAY_SINGLE_BEAM, wmcodecdsp/MICARRAY_SINGLE_CHAN, wmcodecdsp/MIC_ARRAY_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - MIC_ARRAY_MODE
product: Windows
targetos: Windows
req.typenames: MIC_ARRAY_MODE
req.redist: 
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
 

 

