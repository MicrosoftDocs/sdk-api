---
UID: NN:mfmediaengine.IMFMediaEngineEx
title: IMFMediaEngineEx
author: windows-sdk-content
description: Extends the IMFMediaEngine interface.
old-location: mf\imfmediaengineex.htm
tech.root: medfound
ms.assetid: EE3591FD-4FE8-4F20-A4E2-52C896229571
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFMediaEngineEx, IMFMediaEngineEx interface [Media Foundation], IMFMediaEngineEx interface [Media Foundation],described, mf.imfmediaengineex, mfmediaengine/IMFMediaEngineEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx interface


## -description


Extends the <a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineEx</b> interface inherits from <a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>. <b>IMFMediaEngineEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaf8ad21-a790-4a78-b733-b6e3ffd859e1">ApplyStreamSelections</a>
</td>
<td align="left" width="63%">
Applies the stream selections from previous calls to <a href="https://msdn.microsoft.com/12F0FDD0-0D8C-496D-B5C4-3FBCBCAAC6FB">SetStreamSelection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC295919-747B-445D-8C74-E648A612C0BF">CancelTimelineMarkerTimer</a>
</td>
<td align="left" width="63%">
Cancels the next pending timeline marker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B8F2CE8-0963-472F-8C30-AE2BBA844D26">EnableHorizontalMirrorMode</a>
</td>
<td align="left" width="63%">
Enables or disables mirroring of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07128937-bb90-4ed5-85ef-e58c8a273d39">EnableTimeUpdateTimer</a>
</td>
<td align="left" width="63%">
Enables or disables the time update timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B93429D7-A0DF-4440-A164-C140334FC0A6">EnableWindowlessSwapchainMode</a>
</td>
<td align="left" width="63%">
Enables or disables windowless swap-chain mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/090B5B6F-E4D1-43D7-AD09-BA3008B48104">FrameStep</a>
</td>
<td align="left" width="63%">
Steps forward or backward one frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63fa14e-44e6-41b9-a8c9-4b8eb66e98e0">GetAudioEndpointRole</a>
</td>
<td align="left" width="63%">
Gets the audio device endpoint role used for the next  call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/587c0844-93be-42e4-96f6-d5aa721e9ced">GetAudioStreamCategory</a>
</td>
<td align="left" width="63%">
Gets the audio stream category used for the next call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57935B52-27BE-47AF-8702-9DF91E1B515D">GetBalance</a>
</td>
<td align="left" width="63%">
Gets the audio balance.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F3E805A-FE5C-4B75-9333-AE9819CFAFFA">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Gets the number of streams in the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/127667EA-8ED2-428E-8F6B-C280CF42E1C5">GetPresentationAttribute</a>
</td>
<td align="left" width="63%">
Gets a presentation attribute from the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/473a2b5a-5b9d-4754-bd32-89c9c4ab8c4a">GetRealTimeMode</a>
</td>
<td align="left" width="63%">
Gets the real time mode used for the next call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/534595D7-007F-450B-A1C7-FA08F3958417">GetResourceCharacteristics</a>
</td>
<td align="left" width="63%">
Gets various flags that describe the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C2FDE86-2EBD-4A5C-BD02-90613DBFDE65">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets a playback statistic from the Media Engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/003204DB-DDAD-4F72-BA25-015B033BAC92">GetStereo3DFramePackingMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, gets the layout of the two views within a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/204C9B35-860F-46FD-AF3F-7BC7E1EE12EF">GetStereo3DRenderMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, queries how the Media Engine renders the 3D video content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C64CD7B-F376-47DF-AD5A-DE5EBC665288">GetStreamAttribute</a>
</td>
<td align="left" width="63%">
Gets a stream-level attribute from the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93EA1E19-4333-484D-96C8-3244F7C040EF">GetStreamSelection</a>
</td>
<td align="left" width="63%">
Queries whether a stream is selected to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8C58DBB6-A55E-4992-B4F2-EB36E15FA7A1">GetTimelineMarkerTimer</a>
</td>
<td align="left" width="63%">
Gets the time of the next timeline marker, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23AE2296-F0BF-4060-9849-F6A0E0C13B86">GetVideoSwapchainHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the windowless swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D9ED497-A991-473F-A775-CA780A1E0E06">InsertAudioEffect</a>
</td>
<td align="left" width="63%">
Inserts an audio effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F59BE62-D3F1-4C5A-94FD-F864342797BF">InsertVideoEffect</a>
</td>
<td align="left" width="63%">
Inserts a video effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2BE9954A-0B67-45A8-9B79-1148DCB4DDC4">IsPlaybackRateSupported</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine can play at a specified playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/704C469D-C8C7-48D7-B41E-4475B4A9181D">IsProtected</a>
</td>
<td align="left" width="63%">
Queries whether the media resource contains protected content.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9E1C2E47-416F-4016-A576-7BE360A66A81">IsStereo3D</a>
</td>
<td align="left" width="63%">
Queries whether the media resource contains stereoscopic 3D video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B9EF1440-27DA-48C6-B840-FF61DBF19E63">RemoveAllEffects</a>
</td>
<td align="left" width="63%">
Removes all audio and video effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00fd78ce-e046-40a0-8bad-f4a1e1f517bb">SetAudioEndpointRole</a>
</td>
<td align="left" width="63%">
Sets the audio device endpoint used for the next call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55906e89-4064-4355-ad44-7d7d973ddb2c">SetAudioStreamCategory</a>
</td>
<td align="left" width="63%">
Sets the audio stream category for the next call to  <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11187826-B873-4182-A77B-FD9CCECFBAE5">SetBalance</a>
</td>
<td align="left" width="63%">
Sets the audio balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee594f0c-af49-44c2-8c68-16120f76c5e1">SetCurrentTimeEx</a>
</td>
<td align="left" width="63%">
Seeks to a new playback position using the  specified <a href="https://msdn.microsoft.com/58356FC2-5F1E-463F-98D5-E63AFCC05A02">MF_MEDIA_ENGINE_SEEK_MODE</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31534f69-33ec-41d3-93aa-f4c457649e48">SetRealTimeMode</a>
</td>
<td align="left" width="63%">
Sets the real time mode used for the next call to  <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F643383E-AABA-4F32-BCE9-0AA4FD635A0F">SetSourceFromByteStream</a>
</td>
<td align="left" width="63%">
Opens a media resource from a byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E6B1EFA3-188E-495C-A38C-9CD48214BD23">SetStereo3DFramePackingMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, sets the layout of the two views within a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89B6B2AC-A721-4C56-BF0A-A19350FE4823">SetStereo3DRenderMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, specifies how the Media Engine renders the 3D video content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12F0FDD0-0D8C-496D-B5C4-3FBCBCAAC6FB">SetStreamSelection</a>
</td>
<td align="left" width="63%">
Selects or deselects a stream for playback.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2FD65E4A-C70A-4CB4-9038-3A8B791E251C">SetTimelineMarkerTimer</a>
</td>
<td align="left" width="63%">
Specifies a presentation time when the Media Engine will send a marker event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2A9EB449-ED76-4E2C-BC55-20E134B43B43">UpdateVideoStream</a>
</td>
<td align="left" width="63%">
Updates the source rectangle, destination rectangle, and border color for the video.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a> interface contains methods that map to the HTML5 media elements. The <b>IMFMediaEngineEx</b> provides additional functionality that does not correspond directly to HTML5.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=241429">Media Engine Sample</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

