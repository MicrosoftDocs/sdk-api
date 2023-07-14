---
UID: NF:mpeg2data.IMpeg2Stream.Initialize
title: IMpeg2Stream::Initialize (mpeg2data.h)
description: The Initialize method initializes the MPEG2Stream object. This method should be called once, immediately after creating the object. The IMpeg2Data::GetStreamOfSections method calls this method internally, so typically an application will not call it.
helpviewer_keywords: ["IMpeg2Stream interface [Microsoft TV Technologies]","Initialize method","IMpeg2Stream.Initialize","IMpeg2Stream::Initialize","IMpeg2StreamInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IMpeg2Stream interface","mpeg2data/IMpeg2Stream::Initialize","mstv.impeg2stream_initialize"]
old-location: mstv\impeg2stream_initialize.htm
tech.root: mstv
ms.assetid: a2ef2ebc-55dc-49d4-a5de-18203de113ce
ms.date: 12/05/2018
ms.keywords: IMpeg2Stream interface [Microsoft TV Technologies],Initialize method, IMpeg2Stream.Initialize, IMpeg2Stream::Initialize, IMpeg2StreamInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IMpeg2Stream interface, mpeg2data/IMpeg2Stream::Initialize, mstv.impeg2stream_initialize
req.header: mpeg2data.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMpeg2Stream::Initialize
 - mpeg2data/IMpeg2Stream::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2Stream.Initialize
---

# IMpeg2Stream::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Initialize</b> method initializes the <b>MPEG2Stream</b> object. This method should be called once, immediately after creating the object. The <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-getstreamofsections">IMpeg2Data::GetStreamOfSections</a> method calls this method internally, so typically an application will not call it.

## -parameters

### -param requestType [in]

Specifies the request type, as an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ne-mpeg2structs-mpeg_request_type">MPEG_REQUEST_TYPE</a> value.

### -param pMpeg2Data [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.

### -param pContext [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_context">MPEG_CONTEXT</a> structure. This structure indicates the MPEG-2 source.

### -param pid [in]

Specifies a packet identifier (PID), indicating which packets in the transport stream are requested.

### -param tid [in]

Specifies a table identifier (TID), indicating which table sections to retrieve.

### -param pFilter [in]

Optional pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg2_filter">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.

### -param hDataReadyEvent [in]

Handle to an event. The filter signals this event whenever it receives new data.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid or <b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The method has been called on this object already.

</td>
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

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2stream">IMpeg2Stream Interface</a>