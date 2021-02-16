---
UID: NF:wmcontainer.IMFASFStreamSelector.GetBandwidthStepCount
title: IMFASFStreamSelector::GetBandwidthStepCount (wmcontainer.h)
description: Retrieves the number of bandwidth steps that exist for the content. This method is used for multiple bit rate (MBR) content.
helpviewer_keywords: ["6b7105c1-7395-462f-ad52-daf621258714","GetBandwidthStepCount","GetBandwidthStepCount method [Media Foundation]","GetBandwidthStepCount method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","GetBandwidthStepCount method","IMFASFStreamSelector.GetBandwidthStepCount","IMFASFStreamSelector::GetBandwidthStepCount","mf.imfasfstreamselector_getbandwidthstepcount","wmcontainer/IMFASFStreamSelector::GetBandwidthStepCount"]
old-location: mf\imfasfstreamselector_getbandwidthstepcount.htm
tech.root: mf
ms.assetid: 6b7105c1-7395-462f-ad52-daf621258714
ms.date: 12/05/2018
ms.keywords: 6b7105c1-7395-462f-ad52-daf621258714, GetBandwidthStepCount, GetBandwidthStepCount method [Media Foundation], GetBandwidthStepCount method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetBandwidthStepCount method, IMFASFStreamSelector.GetBandwidthStepCount, IMFASFStreamSelector::GetBandwidthStepCount, mf.imfasfstreamselector_getbandwidthstepcount, wmcontainer/IMFASFStreamSelector::GetBandwidthStepCount
req.header: wmcontainer.h
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
 - IMFASFStreamSelector::GetBandwidthStepCount
 - wmcontainer/IMFASFStreamSelector::GetBandwidthStepCount
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
 - IMFASFStreamSelector.GetBandwidthStepCount
---

# IMFASFStreamSelector::GetBandwidthStepCount


## -description

Retrieves the number of bandwidth steps that exist for the content. This method is used for multiple bit rate (MBR) content.

## -parameters

### -param pcStepCount [out]

Receives the number of bandwidth steps.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Bandwidth steps are bandwidth levels used for multiple bit rate (MBR) content. If you stream MBR content, you can choose the bandwidth step that matches the network conditions to avoid interruptions during playback.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstep">IMFASFStreamSelector::GetBandwidthStep</a>