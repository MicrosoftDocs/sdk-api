---
UID: NF:sbe.ISBE2StreamMap.UnmapStream
title: ISBE2StreamMap::UnmapStream (sbe.h)
description: Removes the mapping between a stream and an output pin for a Stream Buffer Source filter.
helpviewer_keywords: ["ISBE2StreamMap interface [Microsoft TV Technologies]","UnmapStream method","ISBE2StreamMap.UnmapStream","ISBE2StreamMap::UnmapStream","UnmapStream","UnmapStream method [Microsoft TV Technologies]","UnmapStream method [Microsoft TV Technologies]","ISBE2StreamMap interface","mstv.isbe2streammap_unmapstream","sbe/ISBE2StreamMap::UnmapStream"]
old-location: mstv\isbe2streammap_unmapstream.htm
tech.root: mstv
ms.assetid: 75736e65-b708-4162-836d-7694899d23d7
ms.date: 12/05/2018
ms.keywords: ISBE2StreamMap interface [Microsoft TV Technologies],UnmapStream method, ISBE2StreamMap.UnmapStream, ISBE2StreamMap::UnmapStream, UnmapStream, UnmapStream method [Microsoft TV Technologies], UnmapStream method [Microsoft TV Technologies],ISBE2StreamMap interface, mstv.isbe2streammap_unmapstream, sbe/ISBE2StreamMap::UnmapStream
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
 - ISBE2StreamMap::UnmapStream
 - sbe/ISBE2StreamMap::UnmapStream
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
 - ISBE2StreamMap.UnmapStream
---

# ISBE2StreamMap::UnmapStream


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Removes the mapping between  a stream and an output pin  for a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter. After a successful call to this method, the output pin stops sending media samples. To resume sending media samples, the pin must be mapped to another stream by a call to the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2streammap-mapstream">MapStream</a> method.

By default, the stream mappings cannot be changed. Before calling this method, disable the default mapping mode by calling the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">ISBE2Crossbar::EnableDefaultMode</a> method without the <b>DEF_MODE_STREAMS</b> flag.

## -parameters

### -param Stream [in]

Identifier for the stream. This stream will be unmapped from the output pin.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified stream does not exist or was not previously mapped to a pin.

</td>
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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot unmap the stream, because the default mode is enabled.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">ISBE2Crossbar::EnableDefaultMode</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2streammap">ISBE2StreamMap </a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2streammap-mapstream">ISBE2StreamMap::MapStream</a>