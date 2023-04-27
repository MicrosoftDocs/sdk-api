---
UID: NE:wmcodecdsp.AEC_SYSTEM_MODE
title: AEC_SYSTEM_MODE (wmcodecdsp.h)
description: Specifies the processing mode for the voice capture DSP. This enumeration is used with the MFPKEY_WMAAECMA_SYSTEM_MODE property.
helpviewer_keywords: ["ADAPTIVE_ARRAY_AND_AEC","ADAPTIVE_ARRAY_ONLY","AEC_SYSTEM_MODE","AEC_SYSTEM_MODE enumeration [Media Foundation]","MODE_NOT_SET","OPTIBEAM_ARRAY_AND_AEC","OPTIBEAM_ARRAY_ONLY","SINGLE_CHANNEL_AEC","SINGLE_CHANNEL_NSAGC","codecapi.aec_system_modeenumeration","mf.aec_system_modeenumeration","wmcodecdsp/ADAPTIVE_ARRAY_AND_AEC","wmcodecdsp/ADAPTIVE_ARRAY_ONLY","wmcodecdsp/AEC_SYSTEM_MODE","wmcodecdsp/MODE_NOT_SET","wmcodecdsp/OPTIBEAM_ARRAY_AND_AEC","wmcodecdsp/OPTIBEAM_ARRAY_ONLY","wmcodecdsp/SINGLE_CHANNEL_AEC","wmcodecdsp/SINGLE_CHANNEL_NSAGC"]
old-location: mf\aec_system_modeenumeration.htm
tech.root: mf
ms.assetid: 637cccba-a2d0-41f4-ac50-eac7e7e29b6b
ms.date: 12/05/2018
ms.keywords: ADAPTIVE_ARRAY_AND_AEC, ADAPTIVE_ARRAY_ONLY, AEC_SYSTEM_MODE, AEC_SYSTEM_MODE enumeration [Media Foundation], MODE_NOT_SET, OPTIBEAM_ARRAY_AND_AEC, OPTIBEAM_ARRAY_ONLY, SINGLE_CHANNEL_AEC, SINGLE_CHANNEL_NSAGC, codecapi.aec_system_modeenumeration, mf.aec_system_modeenumeration, wmcodecdsp/ADAPTIVE_ARRAY_AND_AEC, wmcodecdsp/ADAPTIVE_ARRAY_ONLY, wmcodecdsp/AEC_SYSTEM_MODE, wmcodecdsp/MODE_NOT_SET, wmcodecdsp/OPTIBEAM_ARRAY_AND_AEC, wmcodecdsp/OPTIBEAM_ARRAY_ONLY, wmcodecdsp/SINGLE_CHANNEL_AEC, wmcodecdsp/SINGLE_CHANNEL_NSAGC
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
targetos: Windows
req.typenames: AEC_SYSTEM_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AEC_SYSTEM_MODE
 - wmcodecdsp/AEC_SYSTEM_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - AEC_SYSTEM_MODE
---

# AEC_SYSTEM_MODE enumeration


## -description

Specifies the processing mode for the voice capture DSP. This enumeration is used with the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-system-modeproperty">MFPKEY_WMAAECMA_SYSTEM_MODE </a> property.

## -enum-fields

### -field SINGLE_CHANNEL_AEC:0

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

In all modes, the DSP applies noise suppression and automatic gain control by default. To disable noise suppression, set the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-featr-nsproperty">MFPKEY_WMAAECMA_FEATR_NS</a> property. To disable automatic gain control, set the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-featr-agcproperty">MFPKEY_WMAAECMA_FEATR_AGC</a> property.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/voicecapturedmo">Voice Capture</a>
