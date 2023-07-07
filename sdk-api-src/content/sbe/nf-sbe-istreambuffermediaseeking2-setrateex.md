---
UID: NF:sbe.IStreamBufferMediaSeeking2.SetRateEx
title: IStreamBufferMediaSeeking2::SetRateEx (sbe.h)
description: .
helpviewer_keywords: ["IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies]","SetRateEx method","IStreamBufferMediaSeeking2.SetRateEx","IStreamBufferMediaSeeking2::SetRateEx","IStreamBufferMediaSeeking2SetRateEx","SetRateEx","SetRateEx method [Microsoft TV Technologies]","SetRateEx method [Microsoft TV Technologies]","IStreamBufferMediaSeeking2 interface","mstv.istreambuffermediaseeking2_setrateex","sbe/IStreamBufferMediaSeeking2::SetRateEx"]
old-location: mstv\istreambuffermediaseeking2_setrateex.htm
tech.root: mstv
ms.assetid: 37b80d0d-561d-4ef3-b0ad-70fb43530026
ms.date: 12/05/2018
ms.keywords: IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies],SetRateEx method, IStreamBufferMediaSeeking2.SetRateEx, IStreamBufferMediaSeeking2::SetRateEx, IStreamBufferMediaSeeking2SetRateEx, SetRateEx, SetRateEx method [Microsoft TV Technologies], SetRateEx method [Microsoft TV Technologies],IStreamBufferMediaSeeking2 interface, mstv.istreambuffermediaseeking2_setrateex, sbe/IStreamBufferMediaSeeking2::SetRateEx
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
 - IStreamBufferMediaSeeking2::SetRateEx
 - sbe/IStreamBufferMediaSeeking2::SetRateEx
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
 - IStreamBufferMediaSeeking2.SetRateEx
---

# IStreamBufferMediaSeeking2::SetRateEx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetRateEx</b> method sets the playback rate, and sets the frame rate for fast-forward play ("trick mode").

## -parameters

### -param dRate [in]

Playback rate. Valid range is (<i>dRate</i> &gt;= 0.1 || <i>dRate</i> &lt;= -0.1).

### -param dwFramesPerSec [in]

Frames per second for fast-forward play. Cannot be zero. See Remarks for more information.

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

At higher frames rates, the Stream Buffer Engine drops delta frames and may skip some key frames. This behavior is determined by the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure2-setfftransitionrates">IStreamBufferConfigure2::SetFFTransitionRates</a> method. When the playback rate exceeds the value given in that method's <i>dwMaxNonSkippingRate</i> parameter, the Stream Buffer Engine starts to skip key frames. The number of skipped key frames is determined by the playback rate. To control how many key frames are skipped, use the <b>SetRateEx</b> method:

<ul>
<li>If the playback rate is less than or equal to <i>dwMaxNonSkippingRate</i>, the <i>dwFramesPerSec</i> parameter is ignored.</li>
<li>If the playback rate exceeds <i>dwMaxNonSkippingRate</i>, the Stream Buffer Engine maintains the frame rate specified in <i>dwFramesPerSec</i> and drops key frames if necessary.</li>
</ul>
The frame rate is applied to the video stream. If there is no video stream, the method fails. The actual frame rate may vary over short periods of time.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffermediaseeking2">IStreamBufferMediaSeeking2 Interface</a>