---
UID: NS:dxvahd._DXVAHD_CUSTOM_RATE_DATA
title: DXVAHD_CUSTOM_RATE_DATA (dxvahd.h)
description: Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC). (DXVAHD_CUSTOM_RATE_DATA)
helpviewer_keywords: ["DXVAHD_CUSTOM_RATE_DATA","DXVAHD_CUSTOM_RATE_DATA structure [Media Foundation]","dxvahd/DXVAHD_CUSTOM_RATE_DATA","mf.dxvahd_custom_rate_data"]
old-location: mf\dxvahd_custom_rate_data.htm
tech.root: mf
ms.assetid: 12cac4a8-cfdf-484c-8443-ef47dd3a152b
ms.date: 12/05/2018
ms.keywords: DXVAHD_CUSTOM_RATE_DATA, DXVAHD_CUSTOM_RATE_DATA structure [Media Foundation], dxvahd/DXVAHD_CUSTOM_RATE_DATA, mf.dxvahd_custom_rate_data
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_CUSTOM_RATE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_CUSTOM_RATE_DATA
 - dxvahd/_DXVAHD_CUSTOM_RATE_DATA
 - DXVAHD_CUSTOM_RATE_DATA
 - dxvahd/DXVAHD_CUSTOM_RATE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_CUSTOM_RATE_DATA
---

# DXVAHD_CUSTOM_RATE_DATA structure


## -description

Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC).

## -struct-fields

### -field CustomRate

The ratio of the output frame rate to the input frame rate, expressed as a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_rational">DXVAHD_RATIONAL</a> structure that holds a rational number.

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

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
