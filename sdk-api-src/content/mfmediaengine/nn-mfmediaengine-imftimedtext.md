---
UID: NN:mfmediaengine.IMFTimedText
title: IMFTimedText (mfmediaengine.h)
author: windows-sdk-content
description: A timed-text object represents a component of timed text.
old-location: mf\imftimedtext.htm
tech.root: medfound
ms.assetid: C76D087C-7039-4C1F-93D0-0CBAC925EE43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTimedText, IMFTimedText interface [Media Foundation], IMFTimedText interface [Media Foundation],described, mf.imftimedtext, mfmediaengine/IMFTimedText
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFTimedText"
dev_langs:
 - c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFTimedText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedText interface


## -description


A timed-text object represents a component of timed text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedText</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimedText</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedText</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-adddatasource">AddDataSource</a>
</td>
<td align="left" width="63%">
Adds a timed-text data source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-adddatasourcefromurl">AddDataSourceFromUrl</a>
</td>
<td align="left" width="63%">
Adds a timed-text data source from the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-getactivetracks">GetActiveTracks</a>
</td>
<td align="left" width="63%">
Gets the list of active timed-text tracks in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-getcuetimeoffset">GetCueTimeOffset</a>
</td>
<td align="left" width="63%">
Gets the offset to the cue time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-getmetadatatracks">GetMetadataTracks</a>
</td>
<td align="left" width="63%">
Gets the list of the timed-metadata tracks in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-gettexttracks">GetTextTracks</a>
</td>
<td align="left" width="63%">
Gets the list of all the timed-text tracks in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-gettracks">GetTracks</a>
</td>
<td align="left" width="63%">
Retrieves a list of all timed-text tracks registered with the <b>IMFTimedText</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-isinbandenabled">IsInBandEnabled</a>
</td>
<td align="left" width="63%">
Determines whether inband mode is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-registernotifications">RegisterNotifications</a>
</td>
<td align="left" width="63%">
Registers a timed-text notify object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-removetrack">RemoveTrack</a>
</td>
<td align="left" width="63%">
Removes the timed-text track with the specified identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-selecttrack">SelectTrack</a>
</td>
<td align="left" width="63%">
Selects or deselects a track of text in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-setcuetimeoffset">SetCueTimeOffset</a>
</td>
<td align="left" width="63%">
Sets the offset to the cue time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtext-setinbandenabled">SetInBandEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables inband mode.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

