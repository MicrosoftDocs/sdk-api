---
UID: NF:sbe.ISBE2StreamMap.MapStream
title: ISBE2StreamMap::MapStream (sbe.h)
description: Maps a stream to an output pin for a Stream Buffer Source filter.
helpviewer_keywords: ["ISBE2StreamMap interface [Microsoft TV Technologies]","MapStream method","ISBE2StreamMap.MapStream","ISBE2StreamMap::MapStream","MapStream","MapStream method [Microsoft TV Technologies]","MapStream method [Microsoft TV Technologies]","ISBE2StreamMap interface","mstv.isbe2streammap_mapstream","sbe/ISBE2StreamMap::MapStream"]
old-location: mstv\isbe2streammap_mapstream.htm
tech.root: mstv
ms.assetid: efe3b21d-9664-4367-9bfe-4c02589370c4
ms.date: 12/05/2018
ms.keywords: ISBE2StreamMap interface [Microsoft TV Technologies],MapStream method, ISBE2StreamMap.MapStream, ISBE2StreamMap::MapStream, MapStream, MapStream method [Microsoft TV Technologies], MapStream method [Microsoft TV Technologies],ISBE2StreamMap interface, mstv.isbe2streammap_mapstream, sbe/ISBE2StreamMap::MapStream
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
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
 - ISBE2StreamMap::MapStream
 - sbe/ISBE2StreamMap::MapStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2StreamMap.MapStream
---

# ISBE2StreamMap::MapStream


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Maps a stream to an output pin for a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

By default, the stream mappings cannot be changed. Before calling this method, disable the default mapping mode by calling the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">ISBE2Crossbar::EnableDefaultMode</a> method without the <b>DEF_MODE_STREAMS</b> flag.

## -parameters

### -param Stream [in]

Identifier for the stream mapped to an output pin. The major type of the stream must match the major type of the pin.

## -returns

<table>
<tr>
<th>Return code/value</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The specified stream has already been mapped to a pin.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot unmap the stream, because the default mode is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_NOT_FOUND)</b></dt>
<dt>0x80070490</dt>
</dl>
</td>
<td width="60%">
No stream exists with the specified stream identifier.

</td>
</tr>
</table>

## -remarks

If the new stream has different media type from the previously mapped stream, the output pin follows the dynamic format change procedure described in <a href="/windows/desktop/DirectShow/dynamic-format-changes">Dynamic Format Changes</a>, and flushes downstream pins as described in <a href="/windows/desktop/DirectShow/flushing">Flushing</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">ISBE2Crossbar::EnableDefaultMode</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2streammap">ISBE2StreamMap</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source Filter</a>