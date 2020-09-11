---
UID: NN:d3d11.ID3D11VideoContext
title: ID3D11VideoContext (d3d11.h)
description: Provides the video functionality of a Microsoft Direct3D 11 device.
helpviewer_keywords: ["ID3D11VideoContext","ID3D11VideoContext interface [Media Foundation]","ID3D11VideoContext interface [Media Foundation]","described","d3d11/ID3D11VideoContext","mf.id3d11videocontext"]
old-location: mf\id3d11videocontext.htm
tech.root: mf
ms.assetid: 6EF09C31-56C7-46B5-87AE-B1FE43EC66FC
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext, ID3D11VideoContext interface [Media Foundation], ID3D11VideoContext interface [Media Foundation],described, d3d11/ID3D11VideoContext, mf.id3d11videocontext
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ID3D11VideoContext
 - d3d11/ID3D11VideoContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext
---

# ID3D11VideoContext interface


## -description

Provides the video functionality of a Microsoft Direct3D 11 device.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11VideoContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel">ConfigureAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Sends a configuration command to an authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe">DecoderBeginFrame</a>
</td>
<td align="left" width="63%">
Starts a decoding operation to decode a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe">DecoderEndFrame</a>
</td>
<td align="left" width="63%">
Signals the end of a decoding operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension">DecoderExtension</a>
</td>
<td align="left" width="63%">
Performs an extended function for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt">DecryptionBlt</a>
</td>
<td align="left" width="63%">
Writes encrypted data to a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt">EncryptionBlt</a>
</td>
<td align="left" width="63%">
Reads encrypted data from a protected surface.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh">FinishSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Switches to a new session key.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer">GetDecoderBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a decoder buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey">GetEncryptionBltKey</a>
</td>
<td align="left" width="63%">
Gets the cryptographic key to decrypt the data returned by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt">ID3D11VideoContext::EncryptionBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange">NegotiateAuthenticatedChannelKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes a session key for an authenticated channel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange">NegotiateCryptoSessionKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes the session key for a cryptographic session.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel">QueryAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Sends a query to an authenticated channel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer">ReleaseDecoderBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer">ID3D11VideoContext::GetDecoderBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh">StartSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Gets a random number that can be used to refresh the session key.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers">SubmitDecoderBuffers</a>
</td>
<td align="left" width="63%">
Submits one or more buffers for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">VideoProcessorBlt</a>
</td>
<td align="left" width="63%">
Performs a video processing operation on one or more input samples and writes the result to a Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode">VideoProcessorGetOutputAlphaFillMode</a>
</td>
<td align="left" width="63%">
Gets the current alpha fill mode for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor">VideoProcessorGetOutputBackgroundColor</a>
</td>
<td align="left" width="63%">
Gets the current background color for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace">VideoProcessorGetOutputColorSpace</a>
</td>
<td align="left" width="63%">
Gets the current output color space for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction">VideoProcessorGetOutputConstriction</a>
</td>
<td align="left" width="63%">
Gets the current level of downsampling that is performed by the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension">VideoProcessorGetOutputExtension</a>
</td>
<td align="left" width="63%">
Gets private state data from the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode">VideoProcessorGetOutputStereoMode</a>
</td>
<td align="left" width="63%">
Queries whether the video processor produces stereo video frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect">VideoProcessorGetOutputTargetRect</a>
</td>
<td align="left" width="63%">
Gets the current target rectangle for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha">VideoProcessorGetStreamAlpha</a>
</td>
<td align="left" width="63%">
Gets the planar alpha for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode">VideoProcessorGetStreamAutoProcessingMode</a>
</td>
<td align="left" width="63%">
Queries whether automatic processing features of the video processor are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace">VideoProcessorGetStreamColorSpace</a>
</td>
<td align="left" width="63%">
Gets the color space for an input stream of the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect">VideoProcessorGetStreamDestRect</a>
</td>
<td align="left" width="63%">
Gets the destination rectangle for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension">VideoProcessorGetStreamExtension</a>
</td>
<td align="left" width="63%">
Gets a driver-specific state for a video processing stream.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter">VideoProcessorGetStreamFilter</a>
</td>
<td align="left" width="63%">
Gets the image filter settings for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat">VideoProcessorGetStreamFrameFormat</a>
</td>
<td align="left" width="63%">
Gets the format of an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey">VideoProcessorGetStreamLumaKey</a>
</td>
<td align="left" width="63%">
Gets the luma key for an input stream of the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate">VideoProcessorGetStreamOutputRate</a>
</td>
<td align="left" width="63%">
Gets the rate at which the video processor produces output frames for an input stream.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette">VideoProcessorGetStreamPalette</a>
</td>
<td align="left" width="63%">
Gets the color-palette entries for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio">VideoProcessorGetStreamPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Gets the pixel aspect ratio for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation">VideoProcessorGetStreamRotation</a>
</td>
<td align="left" width="63%">
Gets the stream rotation  for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect">VideoProcessorGetStreamSourceRect</a>
</td>
<td align="left" width="63%">
Gets the source rectangle for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat">VideoProcessorGetStreamStereoFormat</a>
</td>
<td align="left" width="63%">
Gets the stereo 3D format for an input stream on the video processor

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode">VideoProcessorSetOutputAlphaFillMode</a>
</td>
<td align="left" width="63%">
Sets the alpha fill mode for data that the video processor writes to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor">VideoProcessorSetOutputBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace">VideoProcessorSetOutputColorSpace</a>
</td>
<td align="left" width="63%">
Sets the output color space for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction">VideoProcessorSetOutputConstriction</a>
</td>
<td align="left" width="63%">
Sets the amount of downsampling to perform on the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension">VideoProcessorSetOutputExtension</a>
</td>
<td align="left" width="63%">
Sets a driver-specific video processing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode">VideoProcessorSetOutputStereoMode</a>
</td>
<td align="left" width="63%">
Specifies whether the video processor produces stereo video frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect">VideoProcessorSetOutputTargetRect</a>
</td>
<td align="left" width="63%">
Sets the target rectangle for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha">VideoProcessorSetStreamAlpha</a>
</td>
<td align="left" width="63%">
Sets the planar alpha for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode">VideoProcessorSetStreamAutoProcessingMode</a>
</td>
<td align="left" width="63%">
Enables or disables automatic processing features on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace">VideoProcessorSetStreamColorSpace</a>
</td>
<td align="left" width="63%">
Sets the color space for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect">VideoProcessorSetStreamDestRect</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension">VideoProcessorSetStreamExtension</a>
</td>
<td align="left" width="63%">
Sets a driver-specific state on a video processing stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter">VideoProcessorSetStreamFilter</a>
</td>
<td align="left" width="63%">
Enables or disables an image filter for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat">VideoProcessorSetStreamFrameFormat</a>
</td>
<td align="left" width="63%">
Specifies whether an input stream on the video processor contains interlaced or progressive frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey">VideoProcessorSetStreamLumaKey</a>
</td>
<td align="left" width="63%">
Sets the luma key for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate">VideoProcessorSetStreamOutputRate</a>
</td>
<td align="left" width="63%">
Sets the rate at which the video processor produces output frames for an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette">VideoProcessorSetStreamPalette</a>
</td>
<td align="left" width="63%">
Sets the color-palette entries for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio">VideoProcessorSetStreamPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Sets the pixel aspect ratio for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation">VideoProcessorSetStreamRotation</a>
</td>
<td align="left" width="63%">
Sets the stream rotation for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect">VideoProcessorSetStreamSourceRect</a>
</td>
<td align="left" width="63%">
Sets the source rectangle for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">VideoProcessorSetStreamStereoFormat</a>
</td>
<td align="left" width="63%">
Enables or disables stereo 3D video for an input stream on the video processor.

</td>
</tr>
</table>

## -remarks

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface pointer.

This interface provides access to several areas of Microsoft Direct3Dvideo functionality:

<ul>
<li>Hardware-accelerated video decoding</li>
<li>Video processing</li>
<li>GPU-based content protection</li>
<li>Video encryption and decryption</li>
</ul>
In Microsoft Direct3D 9, the equivalent functions were distributed across several interfaces:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9">IDirect3DAuthenticatedChannel9</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>
</li>
</ul>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>

