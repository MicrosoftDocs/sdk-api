---
UID: NF:sbe.IStreamBufferConfigure2.GetFFTransitionRates
title: IStreamBufferConfigure2::GetFFTransitionRates (sbe.h)
description: The GetFFTransitionRates method returns the maximum full-frame and key-frame playback rates.
helpviewer_keywords: ["GetFFTransitionRates","GetFFTransitionRates method [Microsoft TV Technologies]","GetFFTransitionRates method [Microsoft TV Technologies]","IStreamBufferConfigure2 interface","IStreamBufferConfigure2 interface [Microsoft TV Technologies]","GetFFTransitionRates method","IStreamBufferConfigure2.GetFFTransitionRates","IStreamBufferConfigure2::GetFFTransitionRates","IStreamBufferConfigure2GetFFTransitionRates","mstv.istreambufferconfigure2_getfftransitionrates","sbe/IStreamBufferConfigure2::GetFFTransitionRates"]
old-location: mstv\istreambufferconfigure2_getfftransitionrates.htm
tech.root: mstv
ms.assetid: ba0ce9b2-f160-4749-92ba-b9a77f34b980
ms.date: 12/05/2018
ms.keywords: GetFFTransitionRates, GetFFTransitionRates method [Microsoft TV Technologies], GetFFTransitionRates method [Microsoft TV Technologies],IStreamBufferConfigure2 interface, IStreamBufferConfigure2 interface [Microsoft TV Technologies],GetFFTransitionRates method, IStreamBufferConfigure2.GetFFTransitionRates, IStreamBufferConfigure2::GetFFTransitionRates, IStreamBufferConfigure2GetFFTransitionRates, mstv.istreambufferconfigure2_getfftransitionrates, sbe/IStreamBufferConfigure2::GetFFTransitionRates
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferConfigure2::GetFFTransitionRates
 - sbe/IStreamBufferConfigure2::GetFFTransitionRates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure2.GetFFTransitionRates
---

# IStreamBufferConfigure2::GetFFTransitionRates


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetFFTransitionRates</b> method returns the maximum full-frame and key-frame playback rates.

## -parameters

### -param pdwMaxFullFrameRate [out]

Receives the maximum full-frame playback rate. At higher playback rates, only key frames are sent.

### -param pdwMaxNonSkippingRate [out]

Receives the maximum key-frame playback rate. At higher playback rates, some key frames are skipped. The number of key frames that are skipped is proportional to the rate.

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

For more information, see <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure2-setfftransitionrates">IStreamBufferConfigure2::SetFFTransitionRates</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure2">IStreamBufferConfigure2 Interface</a>