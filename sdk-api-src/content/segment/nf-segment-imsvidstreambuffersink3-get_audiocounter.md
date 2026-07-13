---
UID: NF:segment.IMSVidStreamBufferSink3.get_AudioCounter
title: IMSVidStreamBufferSink3::get_AudioCounter (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSink3 interface [Microsoft TV Technologies]","get_AudioCounter method","IMSVidStreamBufferSink3.get_AudioCounter","IMSVidStreamBufferSink3::get_AudioCounter","IMSVidStreamBufferSink3get_AudioCounter","get_AudioCounter","get_AudioCounter method [Microsoft TV Technologies]","get_AudioCounter method [Microsoft TV Technologies]","IMSVidStreamBufferSink3 interface","mstv.imsvidstreambuffersink3_get_audiocounter","segment/IMSVidStreamBufferSink3::get_AudioCounter"]
old-location: mstv\imsvidstreambuffersink3_get_audiocounter.htm
tech.root: mstv
ms.assetid: 8947b90e-4fb6-419a-8207-fa86ec25d40c
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],get_AudioCounter method, IMSVidStreamBufferSink3.get_AudioCounter, IMSVidStreamBufferSink3::get_AudioCounter, IMSVidStreamBufferSink3get_AudioCounter, get_AudioCounter, get_AudioCounter method [Microsoft TV Technologies], get_AudioCounter method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_get_audiocounter, segment/IMSVidStreamBufferSink3::get_AudioCounter
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
 - IMSVidStreamBufferSink3::get_AudioCounter
 - segment/IMSVidStreamBufferSink3::get_AudioCounter
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
 - IMSVidStreamBufferSink3.get_AudioCounter
---

# IMSVidStreamBufferSink3::get_AudioCounter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_AudioCounter</b> method enables the caller to get performance statistics from the Stream Buffer Sink for the audio stream.

## -parameters

### -param ppUnk [out]

Receives a pointer to the <b>IUnknown</b> interface. Query this pointer for the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferdatacounters">IStreamBufferDataCounters</a> interface. The caller must release the <b>IUnknown</b> interface.

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

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersink3">IMSVidStreamBufferSink3 Interface</a>