---
UID: NF:strmif.IDVRGB219.SetRGB219
title: IDVRGB219::SetRGB219 (strmif.h)
description: The SetRGB219 method controls the dynamic range for DV encoding and decoding.
helpviewer_keywords: ["IDVRGB219 interface [DirectShow]","SetRGB219 method","IDVRGB219.SetRGB219","IDVRGB219::SetRGB219","IDVRGB219SetRGB219","SetRGB219","SetRGB219 method [DirectShow]","SetRGB219 method [DirectShow]","IDVRGB219 interface","dshow.idvrgb219_setrgb219","strmif/IDVRGB219::SetRGB219"]
old-location: dshow\idvrgb219_setrgb219.htm
tech.root: dshow
ms.assetid: d203158b-4c15-4fde-9bc2-6d0ba04af504
ms.date: 12/05/2018
ms.keywords: IDVRGB219 interface [DirectShow],SetRGB219 method, IDVRGB219.SetRGB219, IDVRGB219::SetRGB219, IDVRGB219SetRGB219, SetRGB219, SetRGB219 method [DirectShow], SetRGB219 method [DirectShow],IDVRGB219 interface, dshow.idvrgb219_setrgb219, strmif/IDVRGB219::SetRGB219
f1_keywords:
- strmif/IDVRGB219.SetRGB219
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDVRGB219.SetRGB219
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVRGB219::SetRGB219


## -description



The <code>SetRGB219</code> method controls the dynamic range for DV encoding and decoding.



The DV video format has a dynamic range of 16–235. By default, when the DV Video Decoder decodes to 24-bit or 32-bit RGB, it stretches the color range to 0–255. Similarly, the DV Video Encoder compresses 24-bit RGB into the 16-235 range. In RGB-219 mode, the decoder does not stretch the color range, and the encoder does not compress the color range. Use the <code>SetRGB219</code> method to toggle between the default mode and RGB-219 mode.


## -parameters




### -param bState [in]

Boolean value that specifies the filter's encoding or decoder behavior.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Enable RGB-219 mode.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Disable RGB-219 mode. Use the default mode.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> failure code.




## -remarks



For the encoder, this method has no effect unless the input type is RGB-24. For the decoder, it has no effect unless the output type is RGB-24 or RGB-32.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvrgb219">IDVRGB219 Interface</a>
 

 

