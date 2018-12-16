---
UID: NN:mfmediaengine.IMFTimedText
title: IMFTimedText
author: windows-sdk-content
description: A timed-text object represents a component of timed text.
old-location: mf\imftimedtext.htm
tech.root: medfound
ms.assetid: C76D087C-7039-4C1F-93D0-0CBAC925EE43
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFTimedText, IMFTimedText interface [Media Foundation], IMFTimedText interface [Media Foundation],described, mf.imftimedtext, mfmediaengine/IMFTimedText
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedText interface


## -description


A timed-text object represents a component of timed text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedText</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimedText</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/76922DFA-E109-475D-BE09-47501AC7F50E">AddDataSource</a>
</td>
<td align="left" width="63%">
Adds a timed-text data source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5E02BE3F-D0A8-492D-BBB2-F5A95B9C406D">AddDataSourceFromUrl</a>
</td>
<td align="left" width="63%">
Adds a timed-text data source from the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DF9EEFD2-E699-4251-9769-D1F940938D45">GetActiveTracks</a>
</td>
<td align="left" width="63%">
Gets the list of active timed-text tracks in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7619B18-6253-41CF-9D4D-F7944A8E5DDE">GetCueTimeOffset</a>
</td>
<td align="left" width="63%">
Gets the offset to the cue time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EA4D12F6-D1F0-4DA9-BF80-22C6965CE396">GetMetadataTracks</a>
</td>
<td align="left" width="63%">
Gets the list of the timed-metadata tracks in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75F2874A-67E0-4167-9B5D-A8B90C3509E0">GetTextTracks</a>
</td>
<td align="left" width="63%">
Gets the list of all the timed-text tracks in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ECBC4CD-12A0-493A-A301-1E392F6EC280">GetTracks</a>
</td>
<td align="left" width="63%">
Retrieves a list of all timed-text tracks registered with the <b>IMFTimedText</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21BBA2CE-6732-45BD-B5EC-7DBC4A3123E1">IsInBandEnabled</a>
</td>
<td align="left" width="63%">
Determines whether inband mode is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0C43CD34-22A2-440A-97D5-682D979B52A9">RegisterNotifications</a>
</td>
<td align="left" width="63%">
Registers a timed-text notify object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34B785F6-0B34-431A-91CD-3C2DCEFEDAA4">RemoveTrack</a>
</td>
<td align="left" width="63%">
Removes the timed-text track with the specified identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/868FE620-6FF3-4623-BB61-B47D0290D005">SelectTrack</a>
</td>
<td align="left" width="63%">
Selects or deselects a track of text in the timed-text component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42406E51-546F-4714-9179-E5D676805DDE">SetCueTimeOffset</a>
</td>
<td align="left" width="63%">
Sets the offset to the cue time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4AF63D30-4A91-4DFF-96B9-0A26102B93FE">SetInBandEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables inband mode.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

