---
UID: NN:mfmediaengine.IMFTimedTextCue
title: IMFTimedTextCue (mfmediaengine.h)
description: Represents the timed-text-cue object.
old-location: mf\imftimedtextcue.htm
tech.root: medfound
ms.assetid: 831FA230-D0C4-4115-8447-D882686D80EE
ms.date: 12/05/2018
ms.keywords: IMFTimedTextCue, IMFTimedTextCue interface [Media Foundation], IMFTimedTextCue interface [Media Foundation],described, mf.imftimedtextcue, mfmediaengine/IMFTimedTextCue
f1_keywords:
- mfmediaengine/IMFTimedTextCue
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
- IMFTimedTextCue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextCue interface


## -description


Represents the timed-text-cue object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextCue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimedTextCue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextCue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getcuekind">GetCueKind</a>
</td>
<td align="left" width="63%">
Gets the kind of timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getdata">GetData</a>
</td>
<td align="left" width="63%">
Gets the data content of the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration time of the cue in the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getid">GetId</a>
</td>
<td align="left" width="63%">
Gets the identifier of a timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getline">GetLine</a>
</td>
<td align="left" width="63%">
Gets a line of text in the cue from the index of the line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getlinecount">GetLineCount</a>
</td>
<td align="left" width="63%">
Gets the number of lines of text in the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getoriginalid">GetOriginalId</a>
</td>
<td align="left" width="63%">
Gets the cue identifier that is provided in the text-track data format, if available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getregion">GetRegion</a>
</td>
<td align="left" width="63%">
Gets info about the display region  of the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getstarttime">GetStartTime</a>
</td>
<td align="left" width="63%">
Gets the start time of the cue in the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getstyle">GetStyle</a>
</td>
<td align="left" width="63%">
Gets info about the style  of the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-gettrackid">GetTrackId</a>
</td>
<td align="left" width="63%">
Gets the identifier of the timed-text cue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

