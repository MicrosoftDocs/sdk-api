---
UID: NE:wmcodecdsp.MIC_ARRAY_MODE
title: MIC_ARRAY_MODE (wmcodecdsp.h)
description: Specifies how the voice capture DSP performs microphone array processing. This enumeration is used with the MFPKEY_WMAAECMA_FEATR_MICARR_MODE property.
helpviewer_keywords: ["MICARRAY_EXTERN_BEAM","MICARRAY_FIXED_BEAM","MICARRAY_SIMPLE_SUM","MICARRAY_SINGLE_BEAM","MICARRAY_SINGLE_CHAN","MIC_ARRAY_MODE","MIC_ARRAY_MODE enumeration [Media Foundation]","codecapi.mic_array_modeenumeration","mf.mic_array_modeenumeration","wmcodecdsp/MICARRAY_EXTERN_BEAM","wmcodecdsp/MICARRAY_FIXED_BEAM","wmcodecdsp/MICARRAY_SIMPLE_SUM","wmcodecdsp/MICARRAY_SINGLE_BEAM","wmcodecdsp/MICARRAY_SINGLE_CHAN","wmcodecdsp/MIC_ARRAY_MODE"]
old-location: mf\mic_array_modeenumeration.htm
tech.root: mf
ms.assetid: 95335d2e-94f9-4e8d-b578-a4d08055bb56
ms.date: 12/05/2018
ms.keywords: MICARRAY_EXTERN_BEAM, MICARRAY_FIXED_BEAM, MICARRAY_SIMPLE_SUM, MICARRAY_SINGLE_BEAM, MICARRAY_SINGLE_CHAN, MIC_ARRAY_MODE, MIC_ARRAY_MODE enumeration [Media Foundation], codecapi.mic_array_modeenumeration, mf.mic_array_modeenumeration, wmcodecdsp/MICARRAY_EXTERN_BEAM, wmcodecdsp/MICARRAY_FIXED_BEAM, wmcodecdsp/MICARRAY_SIMPLE_SUM, wmcodecdsp/MICARRAY_SINGLE_BEAM, wmcodecdsp/MICARRAY_SINGLE_CHAN, wmcodecdsp/MIC_ARRAY_MODE
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
req.typenames: MIC_ARRAY_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MIC_ARRAY_MODE
 - wmcodecdsp/MIC_ARRAY_MODE
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
 - MIC_ARRAY_MODE
---

# MIC_ARRAY_MODE enumeration


## -description

Specifies how the voice capture DSP performs microphone array processing. This enumeration is used with the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-featr-micarr-modeproperty">MFPKEY_WMAAECMA_FEATR_MICARR_MODE</a> property.

## -enum-fields

### -field MICARRAY_SINGLE_CHAN:0

Use a single channel. Specify the channel number in the last 8 bits of the value.

### -field MICARRAY_SIMPLE_SUM:0x100

Sum all of the channels.

### -field MICARRAY_SINGLE_BEAM:0x200

Use beam forming with a beam selected by the DSP. After processing starts, you can query which beam was selected by reading the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-featr-micarr-beamproperty">MFPKEY_WMAAECMA_FEATR_MICARR_BEAM</a> property.

### -field MICARRAY_FIXED_BEAM:0x400

Use beam forming with the center beam.

### -field MICARRAY_EXTERN_BEAM:0x800

Use beam forming with a beam selected by the application. If you set this value, set the MFPKEY_WMAAECMA_FEATR_MICARR_BEAM property to specify the beam.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/voicecapturedmo">Voice Capture</a>
