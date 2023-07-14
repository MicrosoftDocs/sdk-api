---
UID: NF:segment.IMSVidStreamBufferSource2.put_RateEx
title: IMSVidStreamBufferSource2::put_RateEx (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSource2 interface [Microsoft TV Technologies]","put_RateEx method","IMSVidStreamBufferSource2.put_RateEx","IMSVidStreamBufferSource2::put_RateEx","IMSVidStreamBufferSource2put_RateEx","mstv.imsvidstreambuffersource2_put_rateex","put_RateEx","put_RateEx method [Microsoft TV Technologies]","put_RateEx method [Microsoft TV Technologies]","IMSVidStreamBufferSource2 interface","segment/IMSVidStreamBufferSource2::put_RateEx"]
old-location: mstv\imsvidstreambuffersource2_put_rateex.htm
tech.root: mstv
ms.assetid: b213ad08-8a72-4b4a-bffa-b68783693340
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],put_RateEx method, IMSVidStreamBufferSource2.put_RateEx, IMSVidStreamBufferSource2::put_RateEx, IMSVidStreamBufferSource2put_RateEx, mstv.imsvidstreambuffersource2_put_rateex, put_RateEx, put_RateEx method [Microsoft TV Technologies], put_RateEx method [Microsoft TV Technologies],IMSVidStreamBufferSource2 interface, segment/IMSVidStreamBufferSource2::put_RateEx
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidStreamBufferSource2::put_RateEx
 - segment/IMSVidStreamBufferSource2::put_RateEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSource2.put_RateEx
---

# IMSVidStreamBufferSource2::put_RateEx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>put_RateEx</b> method sets the playback rate, and sets the frame rate for fast-forward play ("trick mode").

## -parameters

### -param dwRate [in]

Playback rate. The valid range is (<i>dRate</i> &gt;= 0.1 || <i>dRate</i> &lt;= –0.1).

### -param dwFramesPerSecond [in]

Frames per second for fast-forward play. For more information, see <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffermediaseeking2-setrateex">IStreamBufferMediaSeeking2::SetRateEx</a>.

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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersource2">IMSVidStreamBufferSource2 Interface</a>