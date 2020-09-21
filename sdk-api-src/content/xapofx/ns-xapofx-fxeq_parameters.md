---
UID: NS:xapofx.FXEQ_PARAMETERS
title: FXEQ_PARAMETERS (xapofx.h)
description: Parameters for use with the FXEQ XAPO.
helpviewer_keywords: ["FXEQ_PARAMETERS","FXEQ_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xapofx/FXEQ_PARAMETERS","xaudio2.fxeq_parameters"]
old-location: xaudio2\fxeq_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapofx.FXEQ_PARAMETERS
ms.date: 12/05/2018
ms.keywords: FXEQ_PARAMETERS, FXEQ_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapofx/FXEQ_PARAMETERS, xaudio2.fxeq_parameters
req.header: xapofx.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FXEQ_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FXEQ_PARAMETERS
 - xapofx/FXEQ_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xapofx.h
api_name:
 - FXEQ_PARAMETERS
---

# FXEQ_PARAMETERS structure


## -description

Parameters for use with the FXEQ XAPO.

## -struct-fields

### -field FrequencyCenter0

Center frequency in Hz for band 0. Must be between FXEQ_MIN_FREQUENCY_CENTER and FXEQ_MAX_FREQUENCY_CENTER.

### -field Gain0

The boost or decrease to frequencies in band 0. Must be between FXEQ_MIN_GAIN and FXEQ_MAX_GAIN

### -field Bandwidth0

Width of band 0. Must be between FXEQ_MIN_BANDWIDTH and FXEQ_MAX_BANDWIDTH.

### -field FrequencyCenter1

Center frequency in Hz for band 1. Must be between FXEQ_MIN_FREQUENCY_CENTER and FXEQ_MAX_FREQUENCY_CENTER.

### -field Gain1

The boost or decrease to frequencies in band 1. Must be between FXEQ_MIN_GAIN and FXEQ_MAX_GAIN

### -field Bandwidth1

Width of band 1. Must be between FXEQ_MIN_BANDWIDTH and FXEQ_MAX_BANDWIDTH.

### -field FrequencyCenter2

Center frequency in Hz for band 2. Must be between FXEQ_MIN_FREQUENCY_CENTER and FXEQ_MAX_FREQUENCY_CENTER.

### -field Gain2

The boost or decrease to frequencies in band 2. Must be between FXEQ_MIN_GAIN and FXEQ_MAX_GAIN

### -field Bandwidth2

Width of band 2. Must be between FXEQ_MIN_BANDWIDTH and FXEQ_MAX_BANDWIDTH.

### -field FrequencyCenter3

Center frequency in Hz for band 3. Must be between FXEQ_MIN_FREQUENCY_CENTER and FXEQ_MAX_FREQUENCY_CENTER.

### -field Gain3

The boost or decrease to frequencies in band 3. Must be between FXEQ_MIN_GAIN and FXEQ_MAX_GAIN

### -field Bandwidth3

Width of band 3. Must be between FXEQ_MIN_BANDWIDTH and FXEQ_MAX_BANDWIDTH.

## -remarks

Each band ranges from <b>FrequencyCenterN</b> - (<b>BandwidthN</b> / 2) to <b>FrequencyCenterN</b> + (<b>BandwidthN</b> / 2).



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>