---
UID: NN:mfplay.IMFPMediaPlayer
title: IMFPMediaPlayer
author: windows-driver-content
description: Contains methods to play media files. (Deprecated.).
old-location: mf\imfpmediaplayer.htm
old-project: medfound
ms.assetid: fa57d465-1ee9-4f7a-9be8-66a6d73f65e8
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFPMediaPlayer, IMFPMediaPlayer interface [Media Foundation], IMFPMediaPlayer interface [Media Foundation], described, mf.imfpmediaplayer, mfplay/IMFPMediaPlayer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplay.h
api_name:
-	IMFPMediaPlayer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer interface


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>



        Contains methods to play media files.

The MFPlay player object exposes this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMediaPlayer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMediaPlayer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMediaPlayer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c2b23ab-b282-445f-a5a0-4291ee6f22ba">ClearMediaItem</a>
</td>
<td align="left" width="63%">
Clears the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">CreateMediaItemFromObject</a>
</td>
<td align="left" width="63%">
Creates a media item from an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">CreateMediaItemFromURL</a>
</td>
<td align="left" width="63%">
Creates a media item from a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7965965-2fbc-4494-9368-7d9699e4092a">FrameStep</a>
</td>
<td align="left" width="63%">
Steps forward one video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaeb20d2-d547-4f88-a69f-7c3f46fe95ff">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Gets the current aspect-ratio correction mode. This mode controls whether the aspect ratio of the video is preserved during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27deeb41-5347-4a6d-bfd4-4e4444540651">GetBalance</a>
</td>
<td align="left" width="63%">
Gets the current audio balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a07bacbd-3d45-4733-a506-3c54ec10b634">GetBorderColor</a>
</td>
<td align="left" width="63%">
Gets the current color of the video border.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d201035-6946-4a46-bc66-b9e78006a04a">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the playback duration of the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6835852-10f0-4453-a22a-a567457bd7c5">GetIdealVideoSize</a>
</td>
<td align="left" width="63%">
Gets the range of video sizes that can be displayed without significantly degrading performance or image quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9593092d-bd50-4ff6-a283-f5a0ab1e6fc0">GetMediaItem</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a628608-37ea-48f3-aed4-0344d47ede9f">GetMute</a>
</td>
<td align="left" width="63%">
Queries whether the audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f0f09fb-d41c-4662-a20c-2a1d04b39df5">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Gets the size and aspect ratio of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3401c66-0dc7-46ef-9a38-088d605a3038">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the current playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51257361-0362-43c4-8aca-81fd49be8482">GetRate</a>
</td>
<td align="left" width="63%">
Gets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/072c5e93-b3ce-469c-8235-3e9c63bd77e3">GetState</a>
</td>
<td align="left" width="63%">
Gets the current playback state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0e738e4-b8e4-41da-8b74-74ce06f17274">GetSupportedRates</a>
</td>
<td align="left" width="63%">
Gets the range of supported playback rates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b72ece3-f573-42e1-948c-443c793e5ba4">GetVideoSourceRect</a>
</td>
<td align="left" width="63%">
Gets the video source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313e3a87-3dad-4cfb-ad37-1018cb03a707">GetVideoWindow</a>
</td>
<td align="left" width="63%">
Gets the window where the video is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08bf0bb3-4ee2-4229-9f41-64924c6122c9">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current audio volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2689ee46-5cfe-4616-850c-eb5aef340daa">InsertEffect</a>
</td>
<td align="left" width="63%">
Applies an audio or video effect to playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24d6e8a0-d910-46f9-8172-dfcb68c4f364">Play</a>
</td>
<td align="left" width="63%">
Starts playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8745714c-315c-4183-86a2-7c189328dfe6">RemoveAllEffects</a>
</td>
<td align="left" width="63%">
Removes all effects that were added with the <a href="https://msdn.microsoft.com/2689ee46-5cfe-4616-850c-eb5aef340daa">IMFPMediaPlayer::InsertEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca8507b9-c6c5-4e17-9c18-3ec1514de897">RemoveEffect</a>
</td>
<td align="left" width="63%">
Removes an effect that was added with the <a href="https://msdn.microsoft.com/2689ee46-5cfe-4616-850c-eb5aef340daa">IMFPMediaPlayer::InsertEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b100a422-548f-4c38-afeb-4d4c1d9a9140">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the aspect ratio of the video is preserved during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb95d037-54b4-4686-b8e6-5b960998d361">SetBalance</a>
</td>
<td align="left" width="63%">
Sets the audio balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f66b671d-0c7d-4261-8210-05f2d2f8d9a5">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the color for the video border.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c792a024-c4f8-4e0b-9720-259d1dc28ee8">SetMediaItem</a>
</td>
<td align="left" width="63%">
Queues a media item for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81e2fb76-a125-4665-9aa5-8971410ee554">SetMute</a>
</td>
<td align="left" width="63%">
Mutes or unmutes the audio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8665c3b-e0da-4a6f-a61b-38d507d1e78a">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e9d4a0d-b61f-47d9-af47-d8a07cd728f6">SetRate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c95d724f-40a9-43c5-b81a-8505eda516f7">SetVideoSourceRect</a>
</td>
<td align="left" width="63%">
Sets the video source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feee2812-7c7e-4c27-86be-8f7316854222">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the audio volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the MFPlay player object and releases any resources that the object is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de583e74-b31b-407e-af4b-c36649e1ca84">UpdateVideo</a>
</td>
<td align="left" width="63%">
Updates the video frame. Call this method when your application receives a <b>WM_PAINT</b> or <b>WM_SIZE</b> message.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

