---
UID: NN:mfmediaengine.IMFTimedTextNotify
title: IMFTimedTextNotify (mfmediaengine.h)
description: Interface that defines callbacks for Microsoft Media Foundation Timed Text notifications.helpviewer_keywords: ["IMFTimedTextNotify","IMFTimedTextNotify interface [Media Foundation]","IMFTimedTextNotify interface [Media Foundation]","described","mf.imftimedtextnotify","mfmediaengine/IMFTimedTextNotify"]
old-location: mf\imftimedtextnotify.htm
tech.root: medfound
ms.assetid: FE782D90-8CD4-4F8B-A20E-CE3F792A2DB4
ms.date: 12/05/2018
ms.keywords: IMFTimedTextNotify, IMFTimedTextNotify interface [Media Foundation], IMFTimedTextNotify interface [Media Foundation],described, mf.imftimedtextnotify, mfmediaengine/IMFTimedTextNotify
f1_keywords:
- mfmediaengine/IMFTimedTextNotify
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
- IMFTimedTextNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextNotify interface


## -description


Interface that defines callbacks  for Microsoft Media Foundation Timed Text notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimedTextNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-cue">Cue</a>
</td>
<td align="left" width="63%">
Called when a cue event occurs in a text track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-error">Error</a>
</td>
<td align="left" width="63%">
Called when an error occurs in a text track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the timed-text-notify object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-trackadded">TrackAdded</a>
</td>
<td align="left" width="63%">
Called when a text track is added

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-trackremoved">TrackRemoved</a>
</td>
<td align="left" width="63%">
Called when a text track is removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-trackselected">TrackSelected</a>
</td>
<td align="left" width="63%">
Called when a track is selected or deselected.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

