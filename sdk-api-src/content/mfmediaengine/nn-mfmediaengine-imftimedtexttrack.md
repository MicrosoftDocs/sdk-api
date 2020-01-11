---
UID: NN:mfmediaengine.IMFTimedTextTrack
title: IMFTimedTextTrack (mfmediaengine.h)
description: Represents a track of timed text.
old-location: mf\imftimedtexttrack.htm
tech.root: medfound
ms.assetid: 55232D19-F3D0-42C7-8B24-C2A7768B2C7E
ms.date: 12/05/2018
ms.keywords: IMFTimedTextTrack, IMFTimedTextTrack interface [Media Foundation], IMFTimedTextTrack interface [Media Foundation],described, mf.imftimedtexttrack, mfmediaengine/IMFTimedTextTrack
f1_keywords:
- mfmediaengine/IMFTimedTextTrack
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
- IMFTimedTextTrack
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextTrack interface


## -description


Represents a track of timed text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextTrack</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimedTextTrack</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getdataformat">GetDataFormat</a>
</td>
<td align="left" width="63%">
Gets a GUID that identifies the track's underlying data format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-geterrorcode">GetErrorCode</a>
</td>
<td align="left" width="63%">
Gets a value indicating the error type of the latest error associated with the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getextendederrorcode">GetExtendedErrorCode</a>
</td>
<td align="left" width="63%">
Gets the extended error code for the latest error associated with the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getid">GetId</a>
</td>
<td align="left" width="63%">
Gets the identifier of the track of timed text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getinbandmetadatatrackdispatchtype">GetInBandMetadataTrackDispatchType</a>
</td>
<td align="left" width="63%">
Gets the in-band metadata of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getlabel">GetLabel</a>
</td>
<td align="left" width="63%">
Gets the label of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getlanguage">GetLanguage</a>
</td>
<td align="left" width="63%">
Gets the language of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-gettrackkind">GetTrackKind</a>
</td>
<td align="left" width="63%">
Gets the kind of timed-text track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-isactive">IsActive</a>
</td>
<td align="left" width="63%">
Determines whether the timed-text track is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-isinband">IsInBand</a>
</td>
<td align="left" width="63%">
Determines whether the timed-text track is inband.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-setlabel">SetLabel</a>
</td>
<td align="left" width="63%">
Sets the label of a timed-text track.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

