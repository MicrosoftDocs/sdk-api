---
UID: NN:mpegtype.IMpegAudioDecoder
title: IMpegAudioDecoder
author: windows-sdk-content
description: The IMpegAudioDecoder interface is exposed on the MPEG-1 Audio Decoder filter and it enables applications to control decoding parameters.
old-location: dshow\impegaudiodecoder.htm
tech.root: DirectShow
ms.assetid: 59fd96ef-2f9a-4a8e-bd08-2695de52b1c6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMpegAudioDecoder, IMpegAudioDecoder interface [DirectShow], IMpegAudioDecoder interface [DirectShow],described, IMpegAudioDecoderInterface, dshow.impegaudiodecoder, mpegtype/IMpegAudioDecoder
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IMpegAudioDecoder interface


## -description



The <code>IMpegAudioDecoder</code> interface is exposed on the <a href="https://msdn.microsoft.com/2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d">MPEG-1 Audio Decoder</a> filter and it enables applications to control decoding parameters. Most of these methods are useful only when an application is running on an older system and needs to sacrifice quality to increase performance. The default values provide the optimal decoding quality.

The two methods that are still useful in some scenarios are <a href="https://msdn.microsoft.com/3b536e8c-91eb-4c32-955f-b343f2c8e16f">get_DualMode</a> and <a href="https://msdn.microsoft.com/b183f669-14bf-44d4-a17d-09cbc593309d">put_DualMode</a>. These methods enable applications to access either the right or left channel in VCD-based karaoke discs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpegAudioDecoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMpegAudioDecoder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f7634504-d3f5-46a9-be25-08293190c27b">get_AudioFormat</a>
</td>
<td align="left" width="63%">
Returns the audio format of the connected input pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b0776f2-4340-4ebc-9d28-a2a2c2a4571e">get_DecoderAccuracy</a>
</td>
<td align="left" width="63%">
Returns the decoder accuracy as a three-level quality setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92528359-cdbf-4490-badd-1ad20643ec1a">get_DecoderWordSize</a>
</td>
<td align="left" width="63%">
Returns the word size used to decode, either eight or 16 bit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b536e8c-91eb-4c32-955f-b343f2c8e16f">get_DualMode</a>
</td>
<td align="left" width="63%">
Returns which channel is currently being decoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b9b2a3f-2495-4da3-8a09-2ba31538bdb0">get_FrequencyDivider</a>
</td>
<td align="left" width="63%">
Returns the frequency divider as a quality setting equal to CD Audio, FM Radio, or AM Radio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cb73c5a-8bca-4dc3-a48c-cac57f3d7fbf">get_IntegerDecode</a>
</td>
<td align="left" width="63%">
Returns whether the decoder is currently using integer-based decoding as opposed to floating point decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb2b4b26-7588-42fd-a915-c09d512cb152">get_Stereo</a>
</td>
<td align="left" width="63%">
Returns whether the decoder is decoding the encoded stream into stereo or mono PCM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fcacbbc-a3e4-4c7b-a9d0-1ecf6a3dca07">put_DecoderAccuracy</a>
</td>
<td align="left" width="63%">
Specifies the quality as high, full or best.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd5ea824-5ac7-44e3-b7db-636e1b350d4e">put_DecoderWordSize</a>
</td>
<td align="left" width="63%">
Specifies the word size used by the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b183f669-14bf-44d4-a17d-09cbc593309d">put_DualMode</a>
</td>
<td align="left" width="63%">
Specifies the channel to be decoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96e5d8f3-b658-408d-a615-e681d8731442">put_FrequencyDivider</a>
</td>
<td align="left" width="63%">
Specifies the frequency divider as a three-level setting corresponding to the quality of CD Audio, FM Radio, or AM Radio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a92fbcbf-0cd5-4c7a-bcde-a616a7d022bd">put_IntegerDecode</a>
</td>
<td align="left" width="63%">
Specifies whether the decoder will use integer-based decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/238e33ba-f35c-423c-be5f-73d1ca14cebd">put_Stereo</a>
</td>
<td align="left" width="63%">
Specifies whether the decoder will decode the encoded stream into stereo or mono PCM.

</td>
</tr>
</table> 

