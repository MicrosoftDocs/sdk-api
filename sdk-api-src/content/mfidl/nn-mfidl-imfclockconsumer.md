---
UID: NN:mfidl.IMFClockConsumer
title: IMFClockConsumer (mfidl.h)
description: Implemented by an app in order to get access to the IMFPresentationClock.
old-location: mf\imfclockconsumer.htm
tech.root: medfound
ms.assetid: B21D3797-695F-4794-80A2-05D381F288C2
ms.date: 12/05/2018
ms.keywords: IMFClockConsumer, IMFClockConsumer interface [Media Foundation], IMFClockConsumer interface [Media Foundation],described, mf.imfclockconsumer, mfidl/IMFClockConsumer
f1_keywords:
- mfidl/IMFClockConsumer
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplat.lib
- mfplat.dll
- mfplat.dll
- mfplat.dll.dll
api_name:
- IMFClockConsumer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFClockConsumer interface


## -description


Implemented by an app in order to get access to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFClockConsumer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFClockConsumer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFClockConsumer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockconsumer-getpresentationclock">GetPresentationClock</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to get an instance of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockconsumer-setpresentationclock">SetPresentationClock</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to provide the app with an instance of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>.

</td>
</tr>
</table> 


## -remarks



The media pipeline checks for the presence of this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a>. Components can use the presentation clock supplied through this interface to determine how much buffering there is in the pipeline after the component. You can do  this in the <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a> method by calculating the difference between the value returned by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime">IMFPresentationClock::GetTime</a> and the value returned by <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime">IMFSample::GetSampleTime</a>. This difference represents the amount of buffered data after the MFT in the pipeline. 



