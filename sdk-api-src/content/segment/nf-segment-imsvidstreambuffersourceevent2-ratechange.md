---
UID: NF:segment.IMSVidStreamBufferSourceEvent2.RateChange
title: IMSVidStreamBufferSourceEvent2::RateChange (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent2 interface [Microsoft TV Technologies]","RateChange method","IMSVidStreamBufferSourceEvent2.RateChange","IMSVidStreamBufferSourceEvent2::RateChange","IMSVidStreamBufferSourceEvent2RateChange","RateChange","RateChange method [Microsoft TV Technologies]","RateChange method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent2 interface","mstv.imsvidstreambuffersourceevent2_ratechange","segment/IMSVidStreamBufferSourceEvent2::RateChange"]
old-location: mstv\imsvidstreambuffersourceevent2_ratechange.htm
tech.root: mstv
ms.assetid: 5c3b9e5f-51ad-4a36-8181-bec4243499a5
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent2 interface [Microsoft TV Technologies],RateChange method, IMSVidStreamBufferSourceEvent2.RateChange, IMSVidStreamBufferSourceEvent2::RateChange, IMSVidStreamBufferSourceEvent2RateChange, RateChange, RateChange method [Microsoft TV Technologies], RateChange method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent2 interface, mstv.imsvidstreambuffersourceevent2_ratechange, segment/IMSVidStreamBufferSourceEvent2::RateChange
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
 - IMSVidStreamBufferSourceEvent2::RateChange
 - segment/IMSVidStreamBufferSourceEvent2::RateChange
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
 - IMSVidStreamBufferSourceEvent2.RateChange
---

# IMSVidStreamBufferSourceEvent2::RateChange


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>RateChange</b> method is called when the playback rate changes.

## -parameters

### -param qwNewRate [in]

Specifies the new playback rate.

### -param qwOldRate [in]

Specifies the previous playback rate.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
</table>

## -remarks

For both parameters, 1.0 represents normal speed. Fractional values are allowed. For example, 0.2 would represent a rate that is slower than normal playback and 1.7 would represent a rate that is faster than normal playback.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent2">IMSVidStreamBufferSourceEvent2 Interface</a>