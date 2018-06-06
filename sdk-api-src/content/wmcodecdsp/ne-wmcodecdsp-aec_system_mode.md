---
UID: NE:wmcodecdsp.AEC_SYSTEM_MODE
title: AEC_SYSTEM_MODE
author: windows-sdk-content
description: Specifies the processing mode for the voice capture DSP. This enumeration is used with the MFPKEY_WMAAECMA_SYSTEM_MODE property.
old-location: mf\aec_system_modeenumeration.htm
old-project: medfound
ms.assetid: 637cccba-a2d0-41f4-ac50-eac7e7e29b6b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ADAPTIVE_ARRAY_AND_AEC, ADAPTIVE_ARRAY_ONLY, AEC_SYSTEM_MODE, AEC_SYSTEM_MODE enumeration [Media Foundation], MODE_NOT_SET, OPTIBEAM_ARRAY_AND_AEC, OPTIBEAM_ARRAY_ONLY, SINGLE_CHANNEL_AEC, SINGLE_CHANNEL_NSAGC, codecapi.aec_system_modeenumeration, mf.aec_system_modeenumeration, wmcodecdsp/ADAPTIVE_ARRAY_AND_AEC, wmcodecdsp/ADAPTIVE_ARRAY_ONLY, wmcodecdsp/AEC_SYSTEM_MODE, wmcodecdsp/MODE_NOT_SET, wmcodecdsp/OPTIBEAM_ARRAY_AND_AEC, wmcodecdsp/OPTIBEAM_ARRAY_ONLY, wmcodecdsp/SINGLE_CHANNEL_AEC, wmcodecdsp/SINGLE_CHANNEL_NSAGC
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
tech.root: 
req.typenames: AEC_SYSTEM_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - AEC_SYSTEM_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

