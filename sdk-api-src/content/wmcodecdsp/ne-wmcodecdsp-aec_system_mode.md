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

# AEC_SYSTEM_MODE enumeration


## -description


Specifies the processing mode for the voice capture DSP. This enumeration is used with the <a href="https://msdn.microsoft.com/479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0">MFPKEY_WMAAECMA_SYSTEM_MODE </a> property.




## -enum-fields




### -field SINGLE_CHANNEL_AEC

AEC processing only.


### -field ADAPTIVE_ARRAY_ONLY

Reserved.


### -field OPTIBEAM_ARRAY_ONLY

Microphone array processing only.




### -field ADAPTIVE_ARRAY_AND_AEC

Reserved.


### -field OPTIBEAM_ARRAY_AND_AEC

Microphone array processing and AEC processing.


### -field SINGLE_CHANNEL_NSAGC

No microphone array processing and no AEC processing.


### -field MODE_NOT_SET

Uninitialized. This value is the initial value of the MFPKEY_WMAAECMA_SYSTEM_MODE property. Do not set this value.




## -remarks



In all modes, the DSP applies noise suppression and automatic gain control by default. To disable noise suppression, set the <a href="https://msdn.microsoft.com/d63e9ac1-9584-4f74-8404-c95d17eb8c2d">MFPKEY_WMAAECMA_FEATR_NS</a> property. To disable automatic gain control, set the <a href="https://msdn.microsoft.com/85ac8de0-ac36-4b34-a93d-0ac792a677b2">MFPKEY_WMAAECMA_FEATR_AGC</a> property.






## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/6c77c8f6-289e-4130-b56a-e1f0bcc40f3e">Voice Capture</a>
 

 

