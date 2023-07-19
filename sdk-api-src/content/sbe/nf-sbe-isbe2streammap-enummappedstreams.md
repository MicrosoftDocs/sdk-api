---
UID: NF:sbe.ISBE2StreamMap.EnumMappedStreams
title: ISBE2StreamMap::EnumMappedStreams (sbe.h)
description: Enumerates streams that are mapped to output pins in a Stream Buffer Source filter.
helpviewer_keywords: ["EnumMappedStreams","EnumMappedStreams method [Microsoft TV Technologies]","EnumMappedStreams method [Microsoft TV Technologies]","ISBE2StreamMap interface","ISBE2StreamMap interface [Microsoft TV Technologies]","EnumMappedStreams method","ISBE2StreamMap.EnumMappedStreams","ISBE2StreamMap::EnumMappedStreams","mstv.isbe2streammap_enummappedstreams","sbe/ISBE2StreamMap::EnumMappedStreams"]
old-location: mstv\isbe2streammap_enummappedstreams.htm
tech.root: mstv
ms.assetid: bb98db94-3aa1-4f29-b98a-7594e27466ef
ms.date: 12/05/2018
ms.keywords: EnumMappedStreams, EnumMappedStreams method [Microsoft TV Technologies], EnumMappedStreams method [Microsoft TV Technologies],ISBE2StreamMap interface, ISBE2StreamMap interface [Microsoft TV Technologies],EnumMappedStreams method, ISBE2StreamMap.EnumMappedStreams, ISBE2StreamMap::EnumMappedStreams, mstv.isbe2streammap_enummappedstreams, sbe/ISBE2StreamMap::EnumMappedStreams
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
 - ISBE2StreamMap::EnumMappedStreams
 - sbe/ISBE2StreamMap::EnumMappedStreams
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
 - ISBE2StreamMap.EnumMappedStreams
---

# ISBE2StreamMap::EnumMappedStreams


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Enumerates streams that are mapped to output pins in a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

## -parameters

### -param ppStreams [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a> interface for an enumeration object that lists all streams mapped to the filter outputs pin.
          The caller is responsible for freeing the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In Windows 7, only one stream at a time can be mapped to an output pin, although a call to the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2streammap-mapstream">ISBE2StreamMap::MapStream</a> method can be used to change the stream mapped to any particular pin while the graph is running. In previous versions of Windows, a stream mapped to a pin could not be changed while the graph was running.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2streammap">ISBE2StreamMap</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source Filter</a>