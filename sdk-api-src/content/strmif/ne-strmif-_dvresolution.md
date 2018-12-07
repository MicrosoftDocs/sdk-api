---
UID: NE:strmif._DVRESOLUTION
title: "_DVRESOLUTION"
author: windows-sdk-content
description: Indicates the digital video (DV) decoding resolution.
old-location: dshow\_dvresolution.htm
tech.root: DirectShow
ms.assetid: 8ae9b402-e7cc-4e11-b956-974b53fd8934
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DVDECODERRESOLUTIONEnumeration, DVRESOLUTION_DC, DVRESOLUTION_FULL, DVRESOLUTION_HALF, DVRESOLUTION_QUARTER, _DVRESOLUTION, _DVRESOLUTION enumeration [DirectShow], dshow._dvresolution, strmif/DVRESOLUTION_DC, strmif/DVRESOLUTION_FULL, strmif/DVRESOLUTION_HALF, strmif/DVRESOLUTION_QUARTER, strmif/_DVRESOLUTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - _DVRESOLUTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _DVRESOLUTION enumeration


## -description



Indicates the digital video (DV) decoding resolution.




## -enum-fields




### -field DVRESOLUTION_FULL

Decode at full size.
          


### -field DVRESOLUTION_HALF

Decode at half size.
          


### -field DVRESOLUTION_QUARTER

Decode at quarter size.
          


### -field DVRESOLUTION_DC

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

<pre class="syntax" xml:space="preserve"><code>enum _DVDECODERRESOLUTION {
    DVDECODERRESOLUTION_720x480     =   1000,
    DVDECODERRESOLUTION_360x240     =   1001,
    DVDECODERRESOLUTION_180x120     =   1002,
    DVDECODERRESOLUTION_88x60       =   1003
};</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/0e40841a-e297-4c05-aefa-7131de9c6a97">IIPDVDec Interface</a>
 

 

