---
UID: NN:mpegtype.IMpegAudioDecoder
title: IMpegAudioDecoder (mpegtype.h)
author: windows-sdk-content
description: The IMpegAudioDecoder interface is exposed on the MPEG-1 Audio Decoder filter and it enables applications to control decoding parameters.
old-location: dshow\impegaudiodecoder.htm
tech.root: DirectShow
ms.assetid: 59fd96ef-2f9a-4a8e-bd08-2695de52b1c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder, IMpegAudioDecoder interface [DirectShow], IMpegAudioDecoder interface [DirectShow],described, IMpegAudioDecoderInterface, dshow.impegaudiodecoder, mpegtype/IMpegAudioDecoder
ms.topic: interface
req.header: mpegtype.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMpegAudioDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpegAudioDecoder interface


## -description



The <code>IMpegAudioDecoder</code> interface is exposed on the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-1-audio-decoder-filter">MPEG-1 Audio Decoder</a> filter and it enables applications to control decoding parameters. Most of these methods are useful only when an application is running on an older system and needs to sacrifice quality to increase performance. The default values provide the optimal decoding quality.

The two methods that are still useful in some scenarios are <a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_dualmode">get_DualMode</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_dualmode">put_DualMode</a>. These methods enable applications to access either the right or left channel in VCD-based karaoke discs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpegAudioDecoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpegAudioDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMpegAudioDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_audioformat">get_AudioFormat</a>
</td>
<td align="left" width="63%">
Returns the audio format of the connected input pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_decoderaccuracy">get_DecoderAccuracy</a>
</td>
<td align="left" width="63%">
Returns the decoder accuracy as a three-level quality setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_decoderwordsize">get_DecoderWordSize</a>
</td>
<td align="left" width="63%">
Returns the word size used to decode, either eight or 16 bit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_dualmode">get_DualMode</a>
</td>
<td align="left" width="63%">
Returns which channel is currently being decoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_frequencydivider">get_FrequencyDivider</a>
</td>
<td align="left" width="63%">
Returns the frequency divider as a quality setting equal to CD Audio, FM Radio, or AM Radio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_integerdecode">get_IntegerDecode</a>
</td>
<td align="left" width="63%">
Returns whether the decoder is currently using integer-based decoding as opposed to floating point decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_stereo">get_Stereo</a>
</td>
<td align="left" width="63%">
Returns whether the decoder is decoding the encoded stream into stereo or mono PCM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_decoderaccuracy">put_DecoderAccuracy</a>
</td>
<td align="left" width="63%">
Specifies the quality as high, full or best.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_decoderwordsize">put_DecoderWordSize</a>
</td>
<td align="left" width="63%">
Specifies the word size used by the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_dualmode">put_DualMode</a>
</td>
<td align="left" width="63%">
Specifies the channel to be decoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_frequencydivider">put_FrequencyDivider</a>
</td>
<td align="left" width="63%">
Specifies the frequency divider as a three-level setting corresponding to the quality of CD Audio, FM Radio, or AM Radio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_integerdecode">put_IntegerDecode</a>
</td>
<td align="left" width="63%">
Specifies whether the decoder will use integer-based decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_stereo">put_Stereo</a>
</td>
<td align="left" width="63%">
Specifies whether the decoder will decode the encoded stream into stereo or mono PCM.

</td>
</tr>
</table> 

