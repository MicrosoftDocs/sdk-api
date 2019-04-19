---
UID: NN:windows.media.streaming.IMediaRenderer
title: IMediaRenderer (windows.media.streaming.h)
author: windows-sdk-content
description: Encapsulates the methods and events needed to represent a DLNA Digital Media Renderer (DMR) device.
old-location: mediastreaming\imediarenderer.htm
tech.root: mediastreaming
ms.assetid: FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaRenderer, IMediaRenderer interface [Media Streaming API], IMediaRenderer interface [Media Streaming API],described, mediastreaming.imediarenderer, windows/IMediaRenderer
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaRenderer interface


## -description


Encapsulates the methods and events  needed to represent a DLNA Digital Media Renderer (DMR) device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaRenderer</b> interface inherits from <a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>. <b>IMediaRenderer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7681FF92-DD13-4BBC-B860-E2BDFDA74FB9">ActionInformation</a>
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
Registers an event handler for the <a href="https://msdn.microsoft.com/863CA879-A420-43D6-9AC8-94F8303BB759">RenderingParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34D11925-387B-414F-A176-336BBCF87821">add_TransportParametersUpdate</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://msdn.microsoft.com/DF9256CA-6C59-462C-B32F-4653546DB384">TransportParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/411CAF71-2888-46A3-8777-80B0D6D9CDE5">GetMuteAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously to determine if audio is currently muted or unmuted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07011C85-34C5-430A-9551-FFC7C24CCED8">GetPositionInformationAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously to retrieve position information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7EA3FB7-0D12-4E49-857F-D8311711AA89">GetTransportInformationAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously to retrieve transport information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CBE8E7EE-DC64-4FB0-B09D-58EC9BACCA26">GetVolumeAsync</a>
</td>
<td align="left" width="63%">
Queries the DMR asynchronously for its current audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5F0C4ED-5778-4388-A7BD-E3923145D663">IsAudioSupported</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of playing audio content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3941789B-0FFF-4F00-B63C-2586B39B6546">IsImageSupported</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of displaying images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE9A14D0-A7A2-4A71-9454-06A05C7D85F9">IsVideoSupported</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of playing video content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B">PauseAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to pause playing the current content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32084664-2D1B-4303-B3B7-9B896A07CB17">PlayAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to play the content that was specified by calling the <a href="https://msdn.microsoft.com/3062FC13-61FD-4781-9AE6-39576D86B783">SetSourceFromUriAsync</a>, <a href="https://msdn.microsoft.com/BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE">SetSourceFromStreamAsync</a>, or <a href="https://msdn.microsoft.com/AC30F3C4-30DD-41B1-B2CE-5F908588A779">SetSourceFromMediaSourceAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/368510CF-FC36-4D92-AE92-024D53EE3BAD">PlayAtSpeedAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to play the content that was specified by calling the <a href="https://msdn.microsoft.com/3062FC13-61FD-4781-9AE6-39576D86B783">SetSourceFromUriAsync</a>, <a href="https://msdn.microsoft.com/BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE">SetSourceFromStreamAsync</a>, or <a href="https://msdn.microsoft.com/AC30F3C4-30DD-41B1-B2CE-5F908588A779">SetSourceFromMediaSourceAsync</a> method at the specified rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5642D180-7FE8-4058-B346-109D5C5817F6">remove_RenderingParametersUpdate</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://msdn.microsoft.com/863CA879-A420-43D6-9AC8-94F8303BB759">RenderingParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7AA7B336-5C51-4774-89A1-F710603A7B23">remove_TransportParametersUpdate</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://msdn.microsoft.com/DF9256CA-6C59-462C-B32F-4653546DB384">TransportParametersUpdate</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3179A942-7756-4763-A2F8-629D89D39542">SeekAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to seek to a particular time offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C043088B-5043-457A-A104-5CE0B228222A">SetMuteAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to either mute or unmute the audio.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/054203C8-766B-4448-A275-CA61C9D177AD">SetNextSourceFromMediaSourceAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/602B4C9B-88A3-4D91-9330-FC02E62F723A">SetNextSourceFromStreamAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6894F1DF-63E2-4091-B61B-736D801E06EF">SetNextSourceFromUriAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing once the current content has finished playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC30F3C4-30DD-41B1-B2CE-5F908588A779">SetSourceFromMediaSourceAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified content for playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE">SetSourceFromStreamAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the specified media stream for playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3062FC13-61FD-4781-9AE6-39576D86B783">SetSourceFromUriAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/422668F3-F5D6-440A-8BF1-A85B17E9A853">SetVolumeAsync</a>
</td>
<td align="left" width="63%">
Sets the audio volume level on the DMR asynchronously to the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0">StopAsync</a>
</td>
<td align="left" width="63%">
Instructs the DMR asynchronously to stop playing the current content.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>
 

 

