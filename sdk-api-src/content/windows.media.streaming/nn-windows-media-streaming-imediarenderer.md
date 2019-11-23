---
UID: NN:windows.media.streaming.IMediaRenderer
title: IMediaRenderer (windows.media.streaming.h)

description: Encapsulates the methods and events needed to represent a DLNA Digital Media Renderer (DMR) device.
old-location: mediastreaming\imediarenderer.htm
tech.root: mediastreaming
ms.assetid: FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB

ms.date: 12/05/2018
ms.keywords: IMediaRenderer, IMediaRenderer interface [Media Streaming API], IMediaRenderer interface [Media Streaming API],described, mediastreaming.imediarenderer, windows/IMediaRenderer
ms.topic: interface
f1_keywords: 
 - "windows.media.streaming/IMediaRenderer"
dev_langs:
 - c++
req.header: windows.media.streaming.h
req.include-header: 
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
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IMediaRenderer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaRenderer interface


## -description


Encapsulates the methods and events  needed to represent a DLNA Digital Media Renderer (DMR) device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaRenderer</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>. <b>IMediaRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-actioninformation">ActionInformation</a>
</td>
<td align="left" width="63%">
Retrieves information about which methods can currently be invoked on the DMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3CEED740-19EA-4CC6-B3F8-F9DE9C6DCC58">add_RenderingParametersUpdate</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/renderingparametersupdate">RenderingParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34D11925-387B-414F-A176-336BBCF87821">add_TransportParametersUpdate</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/transportparametersupdate">TransportParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828930(v=vs.85)">GetMuteAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously to determine if audio is currently muted or unmuted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828931(v=vs.85)">GetPositionInformationAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously to retrieve position information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828932(v=vs.85)">GetTransportInformationAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously to retrieve transport information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828933(v=vs.85)">GetVolumeAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously for its current audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-isaudiosupported">IsAudioSupported</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of playing audio content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-isimagesupported">IsImageSupported</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of displaying images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-isvideosupported">IsVideoSupported</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of playing video content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-pauseasync">PauseAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to pause playing the current content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828938(v=vs.85)">PlayAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to play the content that was specified by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828949(v=vs.85)">SetSourceFromUriAsync</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828948(v=vs.85)">SetSourceFromStreamAsync</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828947(v=vs.85)">SetSourceFromMediaSourceAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828939(v=vs.85)">PlayAtSpeedAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to play the content that was specified by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828949(v=vs.85)">SetSourceFromUriAsync</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828948(v=vs.85)">SetSourceFromStreamAsync</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828947(v=vs.85)">SetSourceFromMediaSourceAsync</a> method at the specified rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828940(v=vs.85)">remove_RenderingParametersUpdate</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/renderingparametersupdate">RenderingParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828941(v=vs.85)">remove_TransportParametersUpdate</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/transportparametersupdate">TransportParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828942(v=vs.85)">SeekAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to seek to a particular time offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828943(v=vs.85)">SetMuteAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to either mute or unmute the audio.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828944(v=vs.85)">SetNextSourceFromMediaSourceAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828945(v=vs.85)">SetNextSourceFromStreamAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828946(v=vs.85)">SetNextSourceFromUriAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing once the current content has finished playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828947(v=vs.85)">SetSourceFromMediaSourceAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified content for playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828948(v=vs.85)">SetSourceFromStreamAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified media stream for playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828949(v=vs.85)">SetSourceFromUriAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828950(v=vs.85)">SetVolumeAsync</a>
</td>
<td align="left" width="63%">
Sets the audio volume level on the DMR asynchronously to the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-stopasync">StopAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to stop playing the current content.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>
 

 

