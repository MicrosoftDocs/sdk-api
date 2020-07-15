---
UID: NN:imapi.IRedbookDiscMaster
title: IRedbookDiscMaster (imapi.h)
description: The IRedbookDiscMaster interface enables the staging of an audio CD image. It represents one of the formats supported by MSDiscMasterObj, and it allows the creation of multi-track audio discs in Track-at-Once mode (fixed-size audio gaps).
helpviewer_keywords: ["IRedbookDiscMaster","IRedbookDiscMaster interface [IMAPI]","IRedbookDiscMaster interface [IMAPI]","described","_win32_iredbookdiscmaster","base.iredbookdiscmaster","imapi.iredbookdiscmaster","imapi/IRedbookDiscMaster"]
old-location: imapi\iredbookdiscmaster.htm
tech.root: imapi
ms.assetid: ea531b22-869a-400e-801f-00bb85ebaac2
ms.date: 12/05/2018
ms.keywords: IRedbookDiscMaster, IRedbookDiscMaster interface [IMAPI], IRedbookDiscMaster interface [IMAPI],described, _win32_iredbookdiscmaster, base.iredbookdiscmaster, imapi.iredbookdiscmaster, imapi/IRedbookDiscMaster
f1_keywords:
- imapi/IRedbookDiscMaster
dev_langs:
- c++
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Actxprxy.dll
api_name:
- IRedbookDiscMaster
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRedbookDiscMaster interface


## -description


The 
<b>IRedbookDiscMaster</b> interface enables the staging of an audio CD image. It represents one of the formats supported by <b>MSDiscMasterObj</b>, and it allows the creation of multi-track audio discs in Track-at-Once mode (fixed-size audio gaps).

Tracks are created in the stash file, data is added to them, and then they are closed. Only one track is staged at a time; this is called the <i>open track</i>. The remaining tracks are closed and committed to the image, while the open track has available to it all the blocks that are not in use by closed tracks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRedbookDiscMaster</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRedbookDiscMaster</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRedbookDiscMaster</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks">AddAudioTrackBlocks</a>
</td>
<td align="left" width="63%">
Adds blocks of audio to a track being staged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack">CloseAudioTrack</a>
</td>
<td align="left" width="63%">
Closes out staging of an audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-createaudiotrack">CreateAudioTrack</a>
</td>
<td align="left" width="63%">
Begins staging a new audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-getaudioblocksize">GetAudioBlockSize</a>
</td>
<td align="left" width="63%">
Retrieves the audio block size in bytes (2352).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks">GetAvailableAudioTrackBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the blocks available for current track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks">GetTotalAudioBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the total audio blocks available on disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-gettotalaudiotracks">GetTotalAudioTracks</a>
</td>
<td align="left" width="63%">
Retrieves the total tracks staged in the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks">GetUsedAudioBlocks</a>
</td>
<td align="left" width="63%">
Retrieves total audio blocks staged in image.

</td>
</tr>
</table> 

