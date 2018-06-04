---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11VideoContext interface


## -description



        Provides the video functionality of a Microsoft Direct3D 11 device. 
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11VideoContext</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6564EC13-A7B3-4A48-8776-4CD46BFF8E8F">ConfigureAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Sends a configuration command to an authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/395B06D8-1BCF-44F2-9F69-A183C30E36B7">DecoderBeginFrame</a>
</td>
<td align="left" width="63%">
Starts a decoding operation to decode a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3596B70C-4BED-49C4-A0E4-8702DA219B01">DecoderEndFrame</a>
</td>
<td align="left" width="63%">
Signals the end of a decoding operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B96FD793-C82A-4752-8F59-3CC9B86D1C2D">DecoderExtension</a>
</td>
<td align="left" width="63%">
Performs an extended function for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E693D97A-E21F-4133-B56A-490F92CBD945">DecryptionBlt</a>
</td>
<td align="left" width="63%">
Writes encrypted data to a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2BBD0BC2-53D9-435E-835C-20A992118329">EncryptionBlt</a>
</td>
<td align="left" width="63%">
Reads encrypted data from a protected surface.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451648">FinishSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Switches to a new session key.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6842D5D7-6165-4428-91BD-2234BE5332B8">GetDecoderBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a decoder buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451660">GetEncryptionBltKey</a>
</td>
<td align="left" width="63%">
Gets the cryptographic key to decrypt the data returned by the <a href="https://msdn.microsoft.com/2BBD0BC2-53D9-435E-835C-20A992118329">ID3D11VideoContext::EncryptionBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451691">NegotiateAuthenticatedChannelKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes a session key for an authenticated channel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76160B03-6F7F-4618-859B-0A7E73540CA4">NegotiateCryptoSessionKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes the session key for a cryptographic session.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E059358-E1FD-4EDB-B1D4-982802385232">QueryAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Sends a query to an authenticated channel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0">ReleaseDecoderBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was obtained by calling the <a href="https://msdn.microsoft.com/6842D5D7-6165-4428-91BD-2234BE5332B8">ID3D11VideoContext::GetDecoderBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451696">StartSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Gets a random number that can be used to refresh the session key.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39010E57-FFF2-4793-B839-E336E8D2C1B2">SubmitDecoderBuffers</a>
</td>
<td align="left" width="63%">
Submits one or more buffers for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451703">VideoProcessorBlt</a>
</td>
<td align="left" width="63%">
Performs a video processing operation on one or more input samples and writes the result to a Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23F37D9C-3D33-4A07-AC54-5273A09BF540">VideoProcessorGetOutputAlphaFillMode</a>
</td>
<td align="left" width="63%">
Gets the current alpha fill mode for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B22666BC-EADF-4812-B299-1EA45F1943C4">VideoProcessorGetOutputBackgroundColor</a>
</td>
<td align="left" width="63%">
Gets the current background color for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26D9C908-D8A6-44F9-895F-48C52F4C8B59">VideoProcessorGetOutputColorSpace</a>
</td>
<td align="left" width="63%">
Gets the current output color space for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40F7D380-C385-4C1C-90E5-E362CA54CD41">VideoProcessorGetOutputConstriction</a>
</td>
<td align="left" width="63%">
Gets the current level of downsampling that is performed by the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451705">VideoProcessorGetOutputExtension</a>
</td>
<td align="left" width="63%">
Gets private state data from the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7BDB9DA-2760-416D-BD51-F73A035B790A">VideoProcessorGetOutputStereoMode</a>
</td>
<td align="left" width="63%">
Queries whether the video processor produces stereo video frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D59822A-B322-4E79-A543-A89C2232C62F">VideoProcessorGetOutputTargetRect</a>
</td>
<td align="left" width="63%">
Gets the current target rectangle for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2DB0672-54D9-4DDB-B6EA-9935237C33FB">VideoProcessorGetStreamAlpha</a>
</td>
<td align="left" width="63%">
Gets the planar alpha for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD7B20C2-5418-4CA5-A64E-FA84D4070A10">VideoProcessorGetStreamAutoProcessingMode</a>
</td>
<td align="left" width="63%">
Queries whether automatic processing features of the video processor are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4D66147C-D4FC-40BC-B406-B40B6EA24D94">VideoProcessorGetStreamColorSpace</a>
</td>
<td align="left" width="63%">
Gets the color space for an input stream of the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F7968C74-8053-4A16-88C7-30729900B95D">VideoProcessorGetStreamDestRect</a>
</td>
<td align="left" width="63%">
Gets the destination rectangle for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439773">VideoProcessorGetStreamExtension</a>
</td>
<td align="left" width="63%">
Gets a driver-specific state for a video processing stream.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E18146E9-FBF4-4A1E-AC6C-7500CDA9DC59">VideoProcessorGetStreamFilter</a>
</td>
<td align="left" width="63%">
Gets the image filter settings for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43879368-1730-4881-B77E-0A975DD5E473">VideoProcessorGetStreamFrameFormat</a>
</td>
<td align="left" width="63%">
Gets the format of an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1DE22456-84E9-478F-A6CA-4C9CACF7E9AF">VideoProcessorGetStreamLumaKey</a>
</td>
<td align="left" width="63%">
Gets the luma key for an input stream of the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69AC0713-FE92-4D89-857A-A0037D51B597">VideoProcessorGetStreamOutputRate</a>
</td>
<td align="left" width="63%">
Gets the rate at which the video processor produces output frames for an input stream.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009568EA-7230-42C0-B35F-AB0A1AF8EC2A">VideoProcessorGetStreamPalette</a>
</td>
<td align="left" width="63%">
Gets the color-palette entries for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45B0CF31-6552-4C75-B32F-755398D1A054">VideoProcessorGetStreamPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Gets the pixel aspect ratio for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6593d829-7f33-408e-aac1-f13e59f7b4bd">VideoProcessorGetStreamRotation</a>
</td>
<td align="left" width="63%">
Gets the stream rotation  for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52AFE959-695B-4797-ABCF-B8264046E4BE">VideoProcessorGetStreamSourceRect</a>
</td>
<td align="left" width="63%">
Gets the source rectangle for an input stream on the video processor.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCEE6C95-C631-4268-9B06-686B8AC7D80C">VideoProcessorGetStreamStereoFormat</a>
</td>
<td align="left" width="63%">
Gets the stereo 3D format for an input stream on the video processor

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439778">VideoProcessorSetOutputAlphaFillMode</a>
</td>
<td align="left" width="63%">
Sets the alpha fill mode for data that the video processor writes to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn459003">VideoProcessorSetOutputBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439782">VideoProcessorSetOutputColorSpace</a>
</td>
<td align="left" width="63%">
Sets the output color space for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439784">VideoProcessorSetOutputConstriction</a>
</td>
<td align="left" width="63%">
Sets the amount of downsampling to perform on the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439786">VideoProcessorSetOutputExtension</a>
</td>
<td align="left" width="63%">
Sets a driver-specific video processing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439788">VideoProcessorSetOutputStereoMode</a>
</td>
<td align="left" width="63%">
Specifies whether the video processor produces stereo video frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439790">VideoProcessorSetOutputTargetRect</a>
</td>
<td align="left" width="63%">
Sets the target rectangle for the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439792">VideoProcessorSetStreamAlpha</a>
</td>
<td align="left" width="63%">
Sets the planar alpha for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439794">VideoProcessorSetStreamAutoProcessingMode</a>
</td>
<td align="left" width="63%">
Enables or disables automatic processing features on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439796">VideoProcessorSetStreamColorSpace</a>
</td>
<td align="left" width="63%">
Sets the color space for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn459004">VideoProcessorSetStreamDestRect</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439800">VideoProcessorSetStreamExtension</a>
</td>
<td align="left" width="63%">
Sets a driver-specific state on a video processing stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439802">VideoProcessorSetStreamFilter</a>
</td>
<td align="left" width="63%">
Enables or disables an image filter for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439804">VideoProcessorSetStreamFrameFormat</a>
</td>
<td align="left" width="63%">
Specifies whether an input stream on the video processor contains interlaced or progressive frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439805">VideoProcessorSetStreamLumaKey</a>
</td>
<td align="left" width="63%">
Sets the luma key for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439807">VideoProcessorSetStreamOutputRate</a>
</td>
<td align="left" width="63%">
Sets the rate at which the video processor produces output frames for an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439809">VideoProcessorSetStreamPalette</a>
</td>
<td align="left" width="63%">
Sets the color-palette entries for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439811">VideoProcessorSetStreamPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Sets the pixel aspect ratio for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439813">VideoProcessorSetStreamRotation</a>
</td>
<td align="left" width="63%">
Sets the stream rotation for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439815">VideoProcessorSetStreamSourceRect</a>
</td>
<td align="left" width="63%">
Sets the source rectangle for an input stream on the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439817">VideoProcessorSetStreamStereoFormat</a>
</td>
<td align="left" width="63%">
Enables or disables stereo 3D video for an input stream on the video processor.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> with an <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface pointer.

This interface provides access to several areas of Microsoft Direct3D
 video functionality:

<ul>
<li>Hardware-accelerated video decoding</li>
<li>Video processing</li>
<li>GPU-based content protection</li>
<li>Video encryption and decryption</li>
</ul>
In Microsoft Direct3D 9, the equivalent functions were distributed across several interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5">IDirectXVideoProcessor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cbfacff5-1cbb-4296-8242-c06b43fc95af">IDXVAHD_VideoProcessor</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

