---
UID: NN:windows.media.streaming.IMediaRendererActionInformation
title: IMediaRendererActionInformation (windows.media.streaming.h)

description: Encapsulates the methods needed to provide information about what methods can currently be invoked on the DMR.
old-location: mediastreaming\imediarendereractioninformation.htm
tech.root: mediastreaming
ms.assetid: 854C7024-D582-405D-8A5F-C152DE8BE0BE

ms.date: 12/05/2018
ms.keywords: IMediaRendererActionInformation, IMediaRendererActionInformation interface [Media Streaming API], IMediaRendererActionInformation interface [Media Streaming API],described, mediastreaming.imediarendereractioninformation, windows/IMediaRendererActionInformation
ms.topic: interface
f1_keywords: 
 - "windows.media.streaming/IMediaRendererActionInformation"
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
 - IMediaRendererActionInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaRendererActionInformation interface


## -description


Encapsulates the methods needed to provide information about what methods can currently be invoked on the DMR.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaRendererActionInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaRendererActionInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaRendererActionInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-ismuteavailable">IsMuteAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of muting the audio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-ispauseavailable">IsPauseAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-pauseasync">PauseAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-isplayavailable">IsPlayAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the accepting the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828938(v=vs.85)">PlayAsync</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828939(v=vs.85)">PlayAtSpeedAsync</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-isseekavailable">IsSeekAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828942(v=vs.85)">SeekAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-issetnextsourceavailable">IsSetNextSourceAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828946(v=vs.85)">SetNextSourceFromUriAsync</a> method, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828945(v=vs.85)">SetNextSourceFromStreamAsync</a> method or the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828944(v=vs.85)">SetNextSourceFromMediaSourceAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-isstopavailable">IsStopAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is currently accepting the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer-stopasync">StopAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-isvolumeavailable">IsVolumeAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendereractioninformation-playspeeds">PlaySpeeds</a>
</td>
<td align="left" width="63%">
Retrieves the complete list of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828990(v=vs.85)">PlaySpeed</a> values that are accepted by the DMR.

</td>
</tr>
</table> 

