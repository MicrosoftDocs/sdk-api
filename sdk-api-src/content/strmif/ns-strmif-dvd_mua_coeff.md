---
UID: NS:strmif.tagDVD_MUA_Coeff
title: DVD_MUA_Coeff (strmif.h)
description: The DVD_MUA_Coeff structure defines the mixing coefficients for one channel in a multichannel audio stream. The DVD_MultichannelAudioAttributes structure contains an array of eight DVD_MUA_Coeff structures, one for each channel in the stream.
helpviewer_keywords: ["DVD_MUA_Coeff","DVD_MUA_Coeff structure [DirectShow]","DVD_MUA_CoeffStructure","dshow.dvd_mua_coeff","strmif/DVD_MUA_Coeff"]
old-location: dshow\dvd_mua_coeff.htm
tech.root: dshow
ms.assetid: 8b8402da-37c2-4983-ae09-967c269fc828
ms.date: 12/05/2018
ms.keywords: DVD_MUA_Coeff, DVD_MUA_Coeff structure [DirectShow], DVD_MUA_CoeffStructure, dshow.dvd_mua_coeff, strmif/DVD_MUA_Coeff
f1_keywords:
- strmif/DVD_MUA_Coeff
dev_langs:
- c++
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
- DVD_MUA_Coeff
targetos: Windows
req.typenames: DVD_MUA_Coeff
req.redist: 
ms.custom: 19H1
---

# DVD_MUA_Coeff structure


## -description



The [DVD_MultichannelAudioAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_multichannelaudioattributes) structure contains an array of eight <code>DVD_MUA_Coeff</code> structures, one for each channel in the stream.




## -struct-fields




### -field log2_alpha

The mixing coefficient for this channel to channel 0.
          


### -field log2_beta

The mixing coefficient for this channel to channel 1.
          


## -remarks



The information contained in this structure reflects the mixing coefficients as authored on the digital video disc (DVD). An application cannot modify these values or otherwise use them unless it is also decoding the audio. In the typical DVD filter graph, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter does not send this information to the decoder.

The alpha coefficient is used to mix to audio channel 0 and the beta coefficient is used to mix to audio channel 1. In general, the following formula calculates the mixing coefficients.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
Audio channel 0 = coeff[0].alpha * value[0] + coeff[1].alpha * value[1] + ... 
Audio channel 1 = coeff[0].beta * value[0]  + coeff[1].beta * value[1] + ... 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




[DVD_AudioAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_audioattributes)



[DVD_MUA_MixingInfo](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_mua_mixinginfo)



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

