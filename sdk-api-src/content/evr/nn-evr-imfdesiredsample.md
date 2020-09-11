---
UID: NN:evr.IMFDesiredSample
title: IMFDesiredSample (evr.h)
description: Enables the presenter for the enhanced video renderer (EVR) to request a specific frame from the video mixer.
helpviewer_keywords: ["373c076c-6329-4332-9f07-f18a01197659","IMFDesiredSample","IMFDesiredSample interface [Media Foundation]","IMFDesiredSample interface [Media Foundation]","described","evr/IMFDesiredSample","mf.imfdesiredsample"]
old-location: mf\imfdesiredsample.htm
tech.root: mf
ms.assetid: 373c076c-6329-4332-9f07-f18a01197659
ms.date: 12/05/2018
ms.keywords: 373c076c-6329-4332-9f07-f18a01197659, IMFDesiredSample, IMFDesiredSample interface [Media Foundation], IMFDesiredSample interface [Media Foundation],described, evr/IMFDesiredSample, mf.imfdesiredsample
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFDesiredSample
 - evr/IMFDesiredSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFDesiredSample
---

# IMFDesiredSample interface


## -description

Enables the presenter for the enhanced video renderer (EVR) to request a specific frame from the video mixer.

The sample objects created by the <a href="https://docs.microsoft.com/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface">MFCreateVideoSampleFromSurface</a> function implement this interface. To retrieve a pointer to this interface, call <b>QueryInterface</b> on the sample.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDesiredSample</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDesiredSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDesiredSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfdesiredsample-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the time stamps previously set by a call to <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration">SetDesiredSampleTimeAndDuration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfdesiredsample-getdesiredsampletimeandduration">GetDesiredSampleTimeAndDuration</a>
</td>
<td align="left" width="63%">
Called by the mixer to get the time and duration of the sample requested by the presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration">SetDesiredSampleTimeAndDuration</a>
</td>
<td align="left" width="63%">
Called by the presenter to set the time and duration of the sample that it requests from the mixer.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

