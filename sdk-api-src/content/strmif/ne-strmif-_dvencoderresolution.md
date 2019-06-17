---
UID: NE:strmif._DVENCODERRESOLUTION
title: "_DVENCODERRESOLUTION" (strmif.h)
author: windows-sdk-content
description: Indicates the digital video (DV) encoding resolution.
old-location: dshow\dvencoderresolution.htm
tech.root: DirectShow
ms.assetid: 110a4510-3a5e-453b-9973-a6cf7e2b0050
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DVENCODERRESOLUTION, DVENCODERRESOLUTIONEnumeration, DVENCODERRESOLUTION_180x120, DVENCODERRESOLUTION_360x240, DVENCODERRESOLUTION_720x480, DVENCODERRESOLUTION_88x60, _DVENCODERRESOLUTION, _DVENCODERRESOLUTION enumeration [DirectShow], dshow.dvencoderresolution, strmif/DVENCODERRESOLUTION_180x120, strmif/DVENCODERRESOLUTION_360x240, strmif/DVENCODERRESOLUTION_720x480, strmif/DVENCODERRESOLUTION_88x60, strmif/_DVENCODERRESOLUTION
ms.topic: enum
f1_keywords: ["strmif/_DVENCODERRESOLUTION"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - _DVENCODERRESOLUTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _DVENCODERRESOLUTION enumeration


## -description



Indicates the digital video (DV) encoding resolution.




## -enum-fields




### -field DVENCODERRESOLUTION_720x480

See Remarks.


### -field DVENCODERRESOLUTION_360x240

See Remarks.


### -field DVENCODERRESOLUTION_180x120

See Remarks.


### -field DVENCODERRESOLUTION_88x60

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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>
 

 

