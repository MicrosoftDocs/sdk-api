---
UID: NF:sbe.ISBE2Crossbar.EnumStreams
title: ISBE2Crossbar::EnumStreams (sbe.h)
description: Gets an enumeration object for all streams that are discovered in a WTV file. The filter crossbar, which exposes the ISBE2Crossbar interface, manages the mappings between the streams in the WTV file and the filter output pins.
helpviewer_keywords: ["EnumStreams","EnumStreams method [Microsoft TV Technologies]","EnumStreams method [Microsoft TV Technologies]","ISBE2Crossbar interface","ISBE2Crossbar interface [Microsoft TV Technologies]","EnumStreams method","ISBE2Crossbar.EnumStreams","ISBE2Crossbar::EnumStreams","mstv.isbe2crossbar_enumstreams","sbe/ISBE2Crossbar::EnumStreams"]
old-location: mstv\isbe2crossbar_enumstreams.htm
tech.root: mstv
ms.assetid: 891dc676-8930-41bc-a0ae-4a080c6d4cd6
ms.date: 12/05/2018
ms.keywords: EnumStreams, EnumStreams method [Microsoft TV Technologies], EnumStreams method [Microsoft TV Technologies],ISBE2Crossbar interface, ISBE2Crossbar interface [Microsoft TV Technologies],EnumStreams method, ISBE2Crossbar.EnumStreams, ISBE2Crossbar::EnumStreams, mstv.isbe2crossbar_enumstreams, sbe/ISBE2Crossbar::EnumStreams
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
 - ISBE2Crossbar::EnumStreams
 - sbe/ISBE2Crossbar::EnumStreams
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
 - ISBE2Crossbar.EnumStreams
---

# ISBE2Crossbar::EnumStreams


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an enumeration object for all streams that are discovered in a WTV file. The filter crossbar, which exposes the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a> interface, manages the mappings between the streams in the WTV file and the filter output pins.

The WTV file format supports dynamic creation and deletion of streams within the file. An <a href="/previous-versions/windows/desktop/api/sbe/ns-sbe-sbe2_stream_desc">SBE2_STREAM_DESC</a> global spanning event in the file signals when a stream is created or deleted.

## -parameters

### -param ppStreams [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a> interface that the crossbar implements.
          You can use the methods that are defined by the <b>ISBE2EnumStream</b>  interface to enumerate the streams that can be mapped to output pins in the current profile. The caller is responsible for releasing the interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
No streams found.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source Filter</a>