---
UID: NN:mfmediaengine.IMFTimedTextTrack
title: IMFTimedTextTrack (mfmediaengine.h)
author: windows-sdk-content
description: Represents a track of timed text.
old-location: mf\imftimedtexttrack.htm
tech.root: medfound
ms.assetid: 55232D19-F3D0-42C7-8B24-C2A7768B2C7E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTimedTextTrack, IMFTimedTextTrack interface [Media Foundation], IMFTimedTextTrack interface [Media Foundation],described, mf.imftimedtexttrack, mfmediaengine/IMFTimedTextTrack
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
 - IMFTimedTextTrack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextTrack interface


## -description


Represents a track of timed text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextTrack</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimedTextTrack</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextTrack</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B00FA013-1C96-48FB-8046-D9A24BB78412">GetDataFormat</a>
</td>
<td align="left" width="63%">
Gets a GUID that identifies the track's underlying data format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D73D3ACC-BD9C-4340-8572-6D82E96D0BA8">GetErrorCode</a>
</td>
<td align="left" width="63%">
Gets a value indicating the error type of the latest error associated with the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61119103-B6F6-414B-AA7E-55DC889A5C28">GetExtendedErrorCode</a>
</td>
<td align="left" width="63%">
Gets the extended error code for the latest error associated with the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0DDC7864-654E-416B-9EF5-4CD47244E8BE">GetId</a>
</td>
<td align="left" width="63%">
Gets the identifier of the track of timed text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AEA4D160-6DBC-4829-95F3-F016F9709042">GetInBandMetadataTrackDispatchType</a>
</td>
<td align="left" width="63%">
Gets the in-band metadata of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BB3B1089-6489-4C70-BAFD-22D72DE3CB38">GetLabel</a>
</td>
<td align="left" width="63%">
Gets the label of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5676082D-A3D2-4239-A73F-65FA77D660EF">GetLanguage</a>
</td>
<td align="left" width="63%">
Gets the language of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B4752EC-553B-42F8-8C8B-52388C803E2E">GetTrackKind</a>
</td>
<td align="left" width="63%">
Gets the kind of timed-text track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7C4A256A-614D-49BF-8654-BEBB4E0A2688">IsActive</a>
</td>
<td align="left" width="63%">
Determines whether the timed-text track is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02B69F41-313A-4792-BB0C-D14A02738002">IsInBand</a>
</td>
<td align="left" width="63%">
Determines whether the timed-text track is inband.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/751CBF14-C445-4F2A-96F6-CB6159FAA1EE">SetLabel</a>
</td>
<td align="left" width="63%">
Sets the label of a timed-text track.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

