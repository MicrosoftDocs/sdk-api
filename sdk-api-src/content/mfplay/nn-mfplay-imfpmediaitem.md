---
UID: NN:mfplay.IMFPMediaItem
title: IMFPMediaItem
author: windows-sdk-content
description: Represents a media item. (Deprecated.).
old-location: mf\imfpmediaitem.htm
tech.root: medfound
ms.assetid: 2839d256-bdaf-40cf-9f9d-46f9e2ce59e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFPMediaItem, IMFPMediaItem interface [Media Foundation], IMFPMediaItem interface [Media Foundation],described, mf.imfpmediaitem, mfplay/IMFPMediaItem
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaItem interface


## -description



<div class="alert"><b>Note</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Represents a media item. A <i>media item</i> is an abstraction for a source of media data, such as a video file. Use this interface to get information about the source, or to change certain playback settings, such as the start and stop times. To get a pointer to this interface, call one of the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">IMFPMediaPlayer::CreateMediaItemFromObject</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMediaItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMediaItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMediaItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fe65644-c7a0-4af5-9765-f933215f5f83">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Gets various flags that describe the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/831f023b-c06f-4099-9f4c-df38f3d1382f">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d6f822a-d599-437e-a73a-2242d4d3fe3a">GetMediaPlayer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the MFPlay player object that created the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/212d468f-de5e-4a55-aaa4-ed487bbf6a00">GetMetadata</a>
</td>
<td align="left" width="63%">
Gets a property store that contains metadata for the source. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Gets the number of streams (audio, video, and other) in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a6abc57-149d-4e4b-a29f-7b712d24e6df">GetObject</a>
</td>
<td align="left" width="63%">
Gets the object that was used to create the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6600009-a8da-4464-9df7-08f20a1a6b15">GetPresentationAttribute</a>
</td>
<td align="left" width="63%">
Queries the media item for a presentation attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c992bbec-a5ca-4ece-a883-2a7d7b5d49b3">GetStartStopPosition</a>
</td>
<td align="left" width="63%">
Gets the start and stop times for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c40ce33-2077-4e7b-8a1c-c080e82df078">GetStreamAttribute</a>
</td>
<td align="left" width="63%">
Queries the media item for a stream attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/808de13b-123f-4b9c-b2e6-6c0a6f4339fc">GetStreamSelection</a>
</td>
<td align="left" width="63%">
Queries whether a stream is selected to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2598534c-28cc-4f4c-bf87-17ab7044e0c1">GetURL</a>
</td>
<td align="left" width="63%">
Gets the URL that was used to create the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa99ced1-c32b-4bf5-b29a-e16eceddfed1">GetUserData</a>
</td>
<td align="left" width="63%">
Gets the application-defined value stored in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38d308d7-77e3-4f13-82e7-677ac94234e7">HasAudio</a>
</td>
<td align="left" width="63%">
Queries whether the media item contains an audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dc8a85c-25e4-4da7-965d-c8882514fc7d">HasVideo</a>
</td>
<td align="left" width="63%">
Queries whether the media item contains a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4ae8b5e-7657-476c-83f9-c27de858e328">IsProtected</a>
</td>
<td align="left" width="63%">
Queries whether the media item contains protected content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f0409a6-1911-47ee-ac65-68b87d6b1db5">SetStartStopPosition</a>
</td>
<td align="left" width="63%">
Sets the start and stop times for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/739190a5-60a7-4b50-9919-f68d2cd6da8d">SetStreamSelection</a>
</td>
<td align="left" width="63%">
Selects or deselects a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97ed9cc0-5f69-4ecb-98c7-c58130b91d7c">SetStreamSink</a>
</td>
<td align="left" width="63%">
Sets a media sink for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17a10427-f13a-494c-bb68-a7722e8d9b6e">SetUserData</a>
</td>
<td align="left" width="63%">
Sets an application-defined value that is stored in the media item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

