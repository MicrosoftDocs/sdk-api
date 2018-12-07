---
UID: NN:d3d11.ID3D11VideoContext
title: ID3D11VideoContext
author: windows-sdk-content
description: Provides the video functionality of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videocontext.htm
tech.root: medfound
ms.assetid: 6EF09C31-56C7-46B5-87AE-B1FE43EC66FC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext, ID3D11VideoContext interface [Media Foundation], ID3D11VideoContext interface [Media Foundation],described, d3d11/ID3D11VideoContext, mf.id3d11videocontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext interface


## -description


Provides the video functionality of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11VideoContext</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh447704(v=VS.85).aspx">ConfigureAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Sends a configuration command to an authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447705(v=VS.85).aspx">DecoderBeginFrame</a>
</td>
<td align="left" width="63%">
Starts a decoding operation to decode a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447706(v=VS.85).aspx">DecoderEndFrame</a>
</td>
<td align="left" width="63%">
Signals the end of a decoding operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447707(v=VS.85).aspx">DecoderExtension</a>
</td>
<td align="left" width="63%">
Performs an extended function for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447708(v=VS.85).aspx">DecryptionBlt</a>
</td>
<td align="left" width="63%">
Writes encrypted data to a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447709(v=VS.85).aspx">EncryptionBlt</a>
</td>
<td align="left" width="63%">
Reads encrypted data from a protected surface.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447710(v=VS.85).aspx">FinishSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Switches to a new session key.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447711(v=VS.85).aspx">GetDecoderBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a decoder buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447712(v=VS.85).aspx">GetEncryptionBltKey</a>
</td>
<td align="left" width="63%">
Gets the cryptographic key to decrypt the data returned by the <a href="https://msdn.microsoft.com/en-us/library/Hh447709(v=VS.85).aspx">ID3D11VideoContext::EncryptionBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447713(v=VS.85).aspx">NegotiateAuthenticatedChannelKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes a session key for an authenticated channel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447714(v=VS.85).aspx">NegotiateCryptoSessionKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes the session key for a cryptographic session.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447715(v=VS.85).aspx">QueryAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Sends a query to an authenticated channel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447716(v=VS.85).aspx">ReleaseDecoderBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Hh447711(v=VS.85).aspx">ID3D11VideoContext::GetDecoderBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447717(v=VS.85).aspx">StartSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Gets a random number that can be used to refresh the session key.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447718(v=VS.85).aspx">SubmitDecoderBuffers</a>
</td>
<td align="left" width="63%">
Submits one or more buffers for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">VideoProcessorBlt</a>
</td>
<td align="left" width="63%">
Performs a video processing operation on one or more input samples and writes the result to a Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447720(v=VS.85).aspx">VideoProcessorGetOutputAlphaFillMode</a>
</td>
<td align="left" width="63%">
Gets the current alpha fill mode for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447721(v=VS.85).aspx">VideoProcessorGetOutputBackgroundColor</a>
</td>
<td align="left" width="63%">
Gets the current background color for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447722(v=VS.85).aspx">VideoProcessorGetOutputColorSpace</a>
</td>
<td align="left" width="63%">
Gets the current output color space for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447723(v=VS.85).aspx">VideoProcessorGetOutputConstriction</a>
</td>
<td align="left" width="63%">
Gets the current level of downsampling that is performed by the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447724(v=VS.85).aspx">VideoProcessorGetOutputExtension</a>
</td>
<td align="left" width="63%">
Gets private state data from the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447725(v=VS.85).aspx">VideoProcessorGetOutputStereoMode</a>
</td>
<td align="left" width="63%">
Queries whether the video processor produces stereo video frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447726(v=VS.85).aspx">VideoProcessorGetOutputTargetRect</a>
</td>
<td align="left" width="63%">
Gets the current target rectangle for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447727(v=VS.85).aspx">VideoProcessorGetStreamAlpha</a>
</td>
<td align="left" width="63%">
Gets the planar alpha for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447729(v=VS.85).aspx">VideoProcessorGetStreamAutoProcessingMode</a>
</td>
<td align="left" width="63%">
Queries whether automatic processing features of the video processor are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447731(v=VS.85).aspx">VideoProcessorGetStreamColorSpace</a>
</td>
<td align="left" width="63%">
Gets the color space for an input stream of the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447733(v=VS.85).aspx">VideoProcessorGetStreamDestRect</a>
</td>
<td align="left" width="63%">
Gets the destination rectangle for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447735(v=VS.85).aspx">VideoProcessorGetStreamExtension</a>
</td>
<td align="left" width="63%">
Gets a driver-specific state for a video processing stream.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447737(v=VS.85).aspx">VideoProcessorGetStreamFilter</a>
</td>
<td align="left" width="63%">
Gets the image filter settings for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447739(v=VS.85).aspx">VideoProcessorGetStreamFrameFormat</a>
</td>
<td align="left" width="63%">
Gets the format of an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447740(v=VS.85).aspx">VideoProcessorGetStreamLumaKey</a>
</td>
<td align="left" width="63%">
Gets the luma key for an input stream of the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447741(v=VS.85).aspx">VideoProcessorGetStreamOutputRate</a>
</td>
<td align="left" width="63%">
Gets the rate at which the video processor produces output frames for an input stream.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447742(v=VS.85).aspx">VideoProcessorGetStreamPalette</a>
</td>
<td align="left" width="63%">
Gets the color-palette entries for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447743(v=VS.85).aspx">VideoProcessorGetStreamPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Gets the pixel aspect ratio for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/JJ160516(v=VS.85).aspx">VideoProcessorGetStreamRotation</a>
</td>
<td align="left" width="63%">
Gets the stream rotation  for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447744(v=VS.85).aspx">VideoProcessorGetStreamSourceRect</a>
</td>
<td align="left" width="63%">
Gets the source rectangle for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447745(v=VS.85).aspx">VideoProcessorGetStreamStereoFormat</a>
</td>
<td align="left" width="63%">
Gets the stereo 3D format for an input stream on the video processor

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447746(v=VS.85).aspx">VideoProcessorSetOutputAlphaFillMode</a>
</td>
<td align="left" width="63%">
Sets the alpha fill mode for data that the video processor writes to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447747(v=VS.85).aspx">VideoProcessorSetOutputBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447748(v=VS.85).aspx">VideoProcessorSetOutputColorSpace</a>
</td>
<td align="left" width="63%">
Sets the output color space for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447749(v=VS.85).aspx">VideoProcessorSetOutputConstriction</a>
</td>
<td align="left" width="63%">
Sets the amount of downsampling to perform on the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447750(v=VS.85).aspx">VideoProcessorSetOutputExtension</a>
</td>
<td align="left" width="63%">
Sets a driver-specific video processing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447751(v=VS.85).aspx">VideoProcessorSetOutputStereoMode</a>
</td>
<td align="left" width="63%">
Specifies whether the video processor produces stereo video frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447752(v=VS.85).aspx">VideoProcessorSetOutputTargetRect</a>
</td>
<td align="left" width="63%">
Sets the target rectangle for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447753(v=VS.85).aspx">VideoProcessorSetStreamAlpha</a>
</td>
<td align="left" width="63%">
Sets the planar alpha for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447754(v=VS.85).aspx">VideoProcessorSetStreamAutoProcessingMode</a>
</td>
<td align="left" width="63%">
Enables or disables automatic processing features on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447755(v=VS.85).aspx">VideoProcessorSetStreamColorSpace</a>
</td>
<td align="left" width="63%">
Sets the color space for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447756(v=VS.85).aspx">VideoProcessorSetStreamDestRect</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447757(v=VS.85).aspx">VideoProcessorSetStreamExtension</a>
</td>
<td align="left" width="63%">
Sets a driver-specific state on a video processing stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447758(v=VS.85).aspx">VideoProcessorSetStreamFilter</a>
</td>
<td align="left" width="63%">
Enables or disables an image filter for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447759(v=VS.85).aspx">VideoProcessorSetStreamFrameFormat</a>
</td>
<td align="left" width="63%">
Specifies whether an input stream on the video processor contains interlaced or progressive frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447760(v=VS.85).aspx">VideoProcessorSetStreamLumaKey</a>
</td>
<td align="left" width="63%">
Sets the luma key for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447761(v=VS.85).aspx">VideoProcessorSetStreamOutputRate</a>
</td>
<td align="left" width="63%">
Sets the rate at which the video processor produces output frames for an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447762(v=VS.85).aspx">VideoProcessorSetStreamPalette</a>
</td>
<td align="left" width="63%">
Sets the color-palette entries for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447763(v=VS.85).aspx">VideoProcessorSetStreamPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Sets the pixel aspect ratio for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/JJ160517(v=VS.85).aspx">VideoProcessorSetStreamRotation</a>
</td>
<td align="left" width="63%">
Sets the stream rotation for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447764(v=VS.85).aspx">VideoProcessorSetStreamSourceRect</a>
</td>
<td align="left" width="63%">
Sets the source rectangle for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447765(v=VS.85).aspx">VideoProcessorSetStreamStereoFormat</a>
</td>
<td align="left" width="63%">
Enables or disables stereo 3D video for an input stream on the video processor.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> with an <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> interface pointer.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd318795(v=VS.85).aspx">IDirect3DAuthenticatedChannel9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd318803(v=VS.85).aspx">IDirect3DCryptoSession9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms694281(v=VS.85).aspx">IDirectXVideoDecoder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms702023(v=VS.85).aspx">IDirectXVideoProcessor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd373918(v=VS.85).aspx">IDXVAHD_VideoProcessor</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn894126(v=VS.85).aspx">ID3D11VideoContext1</a>
 

 

