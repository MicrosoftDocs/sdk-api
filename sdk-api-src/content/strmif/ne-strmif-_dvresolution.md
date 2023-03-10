---
UID: NE:strmif._DVRESOLUTION
title: "_DVRESOLUTION (strmif.h)"
description: Indicates the digital video (DV) decoding resolution.
helpviewer_keywords: ["DVDECODERRESOLUTIONEnumeration","DVRESOLUTION_DC","DVRESOLUTION_FULL","DVRESOLUTION_HALF","DVRESOLUTION_QUARTER","_DVRESOLUTION","_DVRESOLUTION enumeration [DirectShow]","dshow._dvresolution","strmif/DVRESOLUTION_DC","strmif/DVRESOLUTION_FULL","strmif/DVRESOLUTION_HALF","strmif/DVRESOLUTION_QUARTER","strmif/_DVRESOLUTION"]
old-location: dshow\_dvresolution.htm
tech.root: dshow
ms.assetid: 8ae9b402-e7cc-4e11-b956-974b53fd8934
ms.date: 12/05/2018
ms.keywords: DVDECODERRESOLUTIONEnumeration, DVRESOLUTION_DC, DVRESOLUTION_FULL, DVRESOLUTION_HALF, DVRESOLUTION_QUARTER, _DVRESOLUTION, _DVRESOLUTION enumeration [DirectShow], dshow._dvresolution, strmif/DVRESOLUTION_DC, strmif/DVRESOLUTION_FULL, strmif/DVRESOLUTION_HALF, strmif/DVRESOLUTION_QUARTER, strmif/_DVRESOLUTION
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
 - _DVRESOLUTION
 - strmif/_DVRESOLUTION
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
 - _DVRESOLUTION
---

# _DVRESOLUTION enumeration


## -description

Indicates the digital video (DV) decoding resolution.

## -enum-fields

### -field DVRESOLUTION_FULL:1000

Decode at full size.

### -field DVRESOLUTION_HALF:1001

Decode at half size.

### -field DVRESOLUTION_QUARTER:1002

Decode at quarter size.

### -field DVRESOLUTION_DC:1003

Decode at one-eighth size.

## -remarks

The decoding resolution depends on whether the current format is NTSC or PAL:

<table>
<tr>
<th>Enumeration</th>
<th>NTSC</th>
<th>PAL</th>
</tr>
<tr>
<td>DVRESOLUTION_FULL</td>
<td>720 x 480</td>
<td>720 x 576</td>
</tr>
<tr>
<td>DVRESOLUTION_HALF</td>
<td>360 x 240</td>
<td>360 x 288</td>
</tr>
<tr>
<td>DVRESOLUTION_QUARTER</td>
<td>180 x 120</td>
<td>180 x 144</td>
</tr>
<tr>
<td>DVRESOLUTION_DC</td>
<td>88 x 60</td>
<td>88 x 72</td>
</tr>
</table>
 

The following enumeration defined in strmif.h is equivalent to the <b>_DVRESOLUTION</b> enumeration. It is included for compatibility with existing applications.


``` syntax
enum _DVDECODERRESOLUTION {
    DVDECODERRESOLUTION_720x480     =   1000,
    DVDECODERRESOLUTION_360x240     =   1001,
    DVDECODERRESOLUTION_180x120     =   1002,
    DVDECODERRESOLUTION_88x60       =   1003
};
```


## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iipdvdec">IIPDVDec Interface</a>
