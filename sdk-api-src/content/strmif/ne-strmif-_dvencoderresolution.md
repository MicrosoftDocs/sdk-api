---
UID: NE:strmif._DVENCODERRESOLUTION
title: "_DVENCODERRESOLUTION (strmif.h)"
description: Indicates the digital video (DV) encoding resolution.
helpviewer_keywords: ["DVENCODERRESOLUTION","DVENCODERRESOLUTIONEnumeration","DVENCODERRESOLUTION_180x120","DVENCODERRESOLUTION_360x240","DVENCODERRESOLUTION_720x480","DVENCODERRESOLUTION_88x60","_DVENCODERRESOLUTION","_DVENCODERRESOLUTION enumeration [DirectShow]","dshow.dvencoderresolution","strmif/DVENCODERRESOLUTION_180x120","strmif/DVENCODERRESOLUTION_360x240","strmif/DVENCODERRESOLUTION_720x480","strmif/DVENCODERRESOLUTION_88x60","strmif/_DVENCODERRESOLUTION"]
old-location: dshow\dvencoderresolution.htm
tech.root: dshow
ms.assetid: 110a4510-3a5e-453b-9973-a6cf7e2b0050
ms.date: 12/05/2018
ms.keywords: DVENCODERRESOLUTION, DVENCODERRESOLUTIONEnumeration, DVENCODERRESOLUTION_180x120, DVENCODERRESOLUTION_360x240, DVENCODERRESOLUTION_720x480, DVENCODERRESOLUTION_88x60, _DVENCODERRESOLUTION, _DVENCODERRESOLUTION enumeration [DirectShow], dshow.dvencoderresolution, strmif/DVENCODERRESOLUTION_180x120, strmif/DVENCODERRESOLUTION_360x240, strmif/DVENCODERRESOLUTION_720x480, strmif/DVENCODERRESOLUTION_88x60, strmif/_DVENCODERRESOLUTION
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DVENCODERRESOLUTION
 - strmif/_DVENCODERRESOLUTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - _DVENCODERRESOLUTION
---

# _DVENCODERRESOLUTION enumeration


## -description

Indicates the digital video (DV) encoding resolution.

## -enum-fields

### -field DVENCODERRESOLUTION_720x480:2012

See Remarks.

### -field DVENCODERRESOLUTION_360x240:2013

See Remarks.

### -field DVENCODERRESOLUTION_180x120:2014

See Remarks.

### -field DVENCODERRESOLUTION_88x60:2015

See Remarks.

## -remarks

The meaning of the enumeration elements depends on whether the current format is NTSC or PAL:

<table>
<tr>
<th>Element</th>
<th>NTSC</th>
<th>PAL</th>
</tr>
<tr>
<td>DVENCODERRESOLUTION_720x480</td>
<td>720 x 480</td>
<td>720 x 576</td>
</tr>
<tr>
<td>DVENCODERRESOLUTION_360x240</td>
<td>360 x 240</td>
<td>360 x 288</td>
</tr>
<tr>
<td>DVENCODERRESOLUTION_180x120</td>
<td>180 x 120</td>
<td>180 x 144</td>
</tr>
<tr>
<td>DVENCODERRESOLUTION_88x60</td>
<td>88 x 60</td>
<td>88 x 72</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>
