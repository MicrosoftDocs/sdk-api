---
UID: NF:segment.IMSVidStreamBufferSource2.get_VideoCounter
title: IMSVidStreamBufferSource2::get_VideoCounter (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSource2 interface [Microsoft TV Technologies]","get_VideoCounter method","IMSVidStreamBufferSource2.get_VideoCounter","IMSVidStreamBufferSource2::get_VideoCounter","IMSVidStreamBufferSource2get_VideoCounter","get_VideoCounter","get_VideoCounter method [Microsoft TV Technologies]","get_VideoCounter method [Microsoft TV Technologies]","IMSVidStreamBufferSource2 interface","mstv.imsvidstreambuffersource2_get_videocounter","segment/IMSVidStreamBufferSource2::get_VideoCounter"]
old-location: mstv\imsvidstreambuffersource2_get_videocounter.htm
tech.root: mstv
ms.assetid: 9def9b51-bae7-49a2-b32f-61811be63c58
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],get_VideoCounter method, IMSVidStreamBufferSource2.get_VideoCounter, IMSVidStreamBufferSource2::get_VideoCounter, IMSVidStreamBufferSource2get_VideoCounter, get_VideoCounter, get_VideoCounter method [Microsoft TV Technologies], get_VideoCounter method [Microsoft TV Technologies],IMSVidStreamBufferSource2 interface, mstv.imsvidstreambuffersource2_get_videocounter, segment/IMSVidStreamBufferSource2::get_VideoCounter
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
 - IMSVidStreamBufferSource2::get_VideoCounter
 - segment/IMSVidStreamBufferSource2::get_VideoCounter
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
 - IMSVidStreamBufferSource2.get_VideoCounter
---

# IMSVidStreamBufferSource2::get_VideoCounter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_VideoCounter</b> method enables the caller to get performance statistics from the Stream Buffer Source for the video stream.

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

## -remarks

Returns counter interface for the video path

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersource2">IMSVidStreamBufferSource2 Interface</a>