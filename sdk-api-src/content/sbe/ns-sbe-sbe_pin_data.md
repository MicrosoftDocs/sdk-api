---
UID: NS:sbe.SBE_PIN_DATA
title: SBE_PIN_DATA (sbe.h)
description: This topic applies to Windows XP Service Pack 2 only. The STREAMBUFFER_ATTRIBUTE structure contains performance data for the stream buffer filters.
helpviewer_keywords: ["SBE_PIN_DATA","SBE_PIN_DATA structure [Microsoft TV Technologies]","SBE_PIN_DATAStructure","mstv.sbe_pin_data","sbe/SBE_PIN_DATA"]
old-location: mstv\sbe_pin_data.htm
tech.root: mstv
ms.assetid: 727aa921-5156-4b7a-a184-b0744acfa6fb
ms.date: 12/05/2018
ms.keywords: SBE_PIN_DATA, SBE_PIN_DATA structure [Microsoft TV Technologies], SBE_PIN_DATAStructure, mstv.sbe_pin_data, sbe/SBE_PIN_DATA
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: SBE_PIN_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SBE_PIN_DATA
 - sbe/SBE_PIN_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sbe.h
api_name:
 - SBE_PIN_DATA
---

# SBE_PIN_DATA structure


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 2 only.
          

The <b>STREAMBUFFER_ATTRIBUTE</b> structure contains performance data for the stream buffer filters.

## -struct-fields

### -field cDataBytes

Total sample payload, in bytes.

### -field cSamplesProcessed

Number of samples processed.

### -field cDiscontinuities

Number of discontinuities. See <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-setdiscontinuity">IMediaSample::SetDiscontinuity</a>.

### -field cSyncPoints

Number of synchronization points. See <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-setsyncpoint">IMediaSample::SetSyncPoint</a>.

### -field cTimestamps

Number of time stamps.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferdatacounters-getdata">IStreamBufferDataCounters::GetData</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-structures">Stream Buffer Engine Structures</a>