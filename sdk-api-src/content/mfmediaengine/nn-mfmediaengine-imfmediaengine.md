---
UID: NN:mfmediaengine.IMFMediaEngine
title: IMFMediaEngine
author: windows-sdk-content
description: Enables an application to play audio or video files.
old-location: mf\imfmediaengine.htm
tech.root: medfound
ms.assetid: A0023F18-2D28-4F0D-9B00-B8FB11567034
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFMediaEngine, IMFMediaEngine interface [Media Foundation], IMFMediaEngine interface [Media Foundation],described, mf.imfmediaengine, mfmediaengine/IMFMediaEngine
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
 - IMFMediaEngine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine interface


## -description


Enables an application to play audio or video files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngine</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313F631F-7584-4F95-9208-B087CC12010E">CanPlayType</a>
</td>
<td align="left" width="63%">
Queries how likely it is that the Media Engine can play a specified type of media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CEF50308-D4F9-435F-A81A-3746A27846F0">GetAutoPlay</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine automatically begins playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38DABEE7-04AF-4542-AF4D-7988C824EA11">GetBuffered</a>
</td>
<td align="left" width="63%">
Queries how much resource data the media engine has buffered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04C4281D-20ED-49B3-B00C-14ECF1E3BDE1">GetCurrentSource</a>
</td>
<td align="left" width="63%">
Gets the URL of the current media resource, or an empty string if no media resource is present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49FA2383-8AEC-4DDF-8998-25987EEC8223">GetCurrentTime</a>
</td>
<td align="left" width="63%">
Gets the current playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FF7E9E76-B85E-40BB-88BD-5033FCE31177">GetDefaultPlaybackRate</a>
</td>
<td align="left" width="63%">
Gets the default playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E5C793A2-7C6F-42D0-B8DE-17F1B62A0352">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F8A51AF8-8D73-47BC-ADA2-7F5108587873">GetError</a>
</td>
<td align="left" width="63%">
Gets the most recent error status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EBAB4E73-164D-4AE5-87A4-0D37C10071E9">GetLoop</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine will loop playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EDDE60A-1571-4021-B56F-4185694B0911">GetMuted</a>
</td>
<td align="left" width="63%">
Queries whether the audio is muted.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/843F09F7-2E8B-4DF7-AF0C-136BB8626779">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Gets the size of the video frame, adjusted for aspect ratio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7CCA902A-51E9-4B6D-B16C-643177BE1BC9">GetNetworkState</a>
</td>
<td align="left" width="63%">
Gets the current network state of the media engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E270CB86-D90B-43FA-843B-F824970BD4F3">GetPlaybackRate</a>
</td>
<td align="left" width="63%">
Gets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E74D1785-E8BA-4B3A-9FF8-63FBDED5FA9E">GetPlayed</a>
</td>
<td align="left" width="63%">
Gets the time ranges that have been rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA1942B2-C5BB-46F7-B163-1BCB3372D453">GetPreload</a>
</td>
<td align="left" width="63%">
Gets the preload flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B8C9B600-87FD-4DE6-8794-5C1E41449554">GetReadyState</a>
</td>
<td align="left" width="63%">
Gets the ready state, which indicates whether the current media resource can be rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FB238892-B172-4E31-B4E5-68C96E135345">GetSeekable</a>
</td>
<td align="left" width="63%">
Gets the time ranges to which the Media Engine can currently seek.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18793EC9-D04A-443F-8469-44CC00C4EE27">GetStartTime</a>
</td>
<td align="left" width="63%">
Gets the initial playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82B4AD4B-1A2E-4B03-8343-E4E5A43E62D2">GetVideoAspectRatio</a>
</td>
<td align="left" width="63%">
Gets the picture aspect ratio of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7890777-480E-4EA1-88BA-657182B66010">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D06A773E-8D41-40D1-BA10-65AEFF2D7667">HasAudio</a>
</td>
<td align="left" width="63%">
Queries whether the current media resource contains an audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30B7F4DC-B3EB-421B-998B-E098F04D4B33">HasVideo</a>
</td>
<td align="left" width="63%">
Queries whether the current media resource contains a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0760707C-B25E-44FF-9263-6B59BF43A98E">IsEnded</a>
</td>
<td align="left" width="63%">
Queries whether playback has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A2E9C498-FEEB-4506-9E69-59028A6B4EE5">IsPaused</a>
</td>
<td align="left" width="63%">
Queries whether playback is currently paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B314D5E7-EBD4-42CF-9E86-206ABC3027A0">IsSeeking</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine is currently seeking to a new playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>
</td>
<td align="left" width="63%">
Loads the current media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC06D3D6-F103-4932-96C1-B55A59CD5E34">OnVideoStreamTick</a>
</td>
<td align="left" width="63%">
Queries the Media Engine to find out whether a new video frame is ready.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C1FEBDA-18B5-4BF4-9AF4-FF6DBCDD880D">Pause</a>
</td>
<td align="left" width="63%">
Pauses playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">Play</a>
</td>
<td align="left" width="63%">
Starts playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/867FE1D2-39AE-4A44-99DD-98A8ABD234A2">SetAutoPlay</a>
</td>
<td align="left" width="63%">
Specifies whether the Media Engine automatically begins playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C64BCBA0-097E-4035-BFEE-F9EC949B109A">SetCurrentTime</a>
</td>
<td align="left" width="63%">
Seeks to a new playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D6EA6BC1-021A-432D-BBCB-BE2FD15E7BE5">SetDefaultPlaybackRate</a>
</td>
<td align="left" width="63%">
Sets the default playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B40AFD99-1048-44C5-A3FA-ED57720956B4">SetErrorCode</a>
</td>
<td align="left" width="63%">
Sets the current error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0B8890EA-9207-428B-8EC2-18B51E1D8365">SetLoop</a>
</td>
<td align="left" width="63%">
Specifies whether the Media Engine loops playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/330CB3CF-F649-4964-A24D-3C16E778BFD7">SetMuted</a>
</td>
<td align="left" width="63%">
Mutes or unmutes the audio.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/648BF1CC-BFAC-4874-808B-F8B46E3E9989">SetPlaybackRate</a>
</td>
<td align="left" width="63%">
Sets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3480C16F-E4E4-469C-BE27-711044691A49">SetPreload</a>
</td>
<td align="left" width="63%">
Sets the preload flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a>
</td>
<td align="left" width="63%">
Sets the URL of a media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC">SetSourceElements</a>
</td>
<td align="left" width="63%">
Sets a list of media sources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/010EE05C-3F81-404E-8AFB-7C57CA55A8AE">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8B7BCEAC-7A30-4B60-AD0E-E8DCE404DDE9">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the Media Engine and releases the resources it is using.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07DB29E2-9F09-46CB-B138-197D95EC37F0">TransferVideoFrame</a>
</td>
<td align="left" width="63%">
Copies the current video frame to a DXGI surface or WIC bitmap.

</td>
</tr>
</table> 


## -remarks



The Media Engine implements this interface. To create an instance of the Media Engine, call <a href="https://msdn.microsoft.com/EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F">IMFMediaEngineClassFactory::CreateInstance</a>.

This interface is extended with <a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=241429">Media Engine Sample</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

